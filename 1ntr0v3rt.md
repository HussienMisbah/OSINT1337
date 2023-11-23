| challenge name | 1ntr0v3rt |
| -------- | ------- |
| Category | OSINT |
| CTF | Arab Regional Finals 2022 |
| Solves | 2 |
| key concepts | osint process  |
| description | Our introvert co-worker left the company a while ago , she is really missed and we want to contact her. However, all we knew about her is her old twitter handle which was "bye_Agatha". can you help us reach her ? - we also remember she is a real marvel fan if that may help you |

We are given a start point which is the old Twitter handle “bye_Agatha”, we can start from there.
However, Trying to visit the account we will see it doesn’t exist. It seems like it had changed the handle or deleted the account

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/7b84f0e2-8655-4ca7-96aa-eedc202e4700)


As we suspect this handle was old and it has been changed, we can check waybackUrls . we will find one recent  screenshot


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/8554e747-956e-4af4-a286-0ff77f1554ba)


Checking the screenshot we can see the following, it looks like our guess is correct, and she has changed the Twitter handle and username.

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/5b492761-8072-4ab8-8b83-e7cef10b6f87)


Our goal now is to get the new username or handle, the only way we can trace the Twitter account is by knowing the ID. if we open the source code of this screenshot we will find the ID :


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/d8d5a764-aeca-4017-ad11-380c436d0071)


By knowing the ID, we can get the current account using that ID. using online tools


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/894b55d2-186e-4c1e-a2fb-858dc3e8aab5)


Visiting the account using the new handle we just discovered, we can see the handle is ``itssakinahh8971``


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/2aa1da41-db36-48a5-a0b5-91b6c1e5fc51)


The OSINT process requires us to enumerate what we have to get more information. So we can try to check if she is using the same handle on any other platform. We can utilize the sherlock tool to check for that 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/6b9e6e36-64d9-430d-bd19-9ddf7bad974b)


Starting with Github, we can see it has only one Repository, we can see it has some sort of telegram bot. 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/11e426b6-2631-4271-9724-1e40c081de18)


Checking old Commits we can see this deleted part, it seems there is some command that has been removed from the bot which is /s3c3rtcmd it checks for a secret and if matched a redacted value will reveal the flag.

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/313dd419-2103-46fa-9df4-cac1f2f4098c)


So now we know how to retrieve the flag, but we don’t know :
- The bot name
- Required secret

From the sherlock output there is also a potential Trello account we can investigate.

- It looks like it is a member of a public Trello workspace as we can see the activity below

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/a57a881d-9544-49b2-910c-a49fe0458bb7)


We can see a card here talking about some secret

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/b08a8bef-4056-43ae-8b25-d908842c0072)


Checking the card comments will see she has shared a Pastebin link containing some sort of hash (hopefully our required secret for the bot)

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/47298236-71cd-4b17-be73-aa1f72e0673a)



So now we don’t have any more clues to follow for the sakinah user, we can try to go after other users on the Trello board. Maybe her co-workers leaked some information unintentionally.

- We can see the other user in the workspace is michaelschwart22

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/1e31f0f5-c93c-4541-b48d-9dc1d6d837cf)


We can use the sherlock tool again against this user, maybe we find this handle is shared in another platform

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/83771eff-a500-4348-ae72-5a36c87fabec)


We can see that the Instagram account is valid. 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/18ee8d90-0a95-4213-967e-e99b37a48ddb)

Checking it we got no posts but we can see some public highlights one of them contains the bot name.

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/e837360b-d5ce-4d6f-9cee-71f07c59a123)

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/1ba9e9d8-b8ec-47dc-937e-6e4c24359b44)


So now we have the bot name, the secret to reveal the flag, and the hidden command from Github old commits. We are ready to connect to the bot

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/ea4e97d6-4a7d-4f58-a6f9-91d7aeb5ed93)
