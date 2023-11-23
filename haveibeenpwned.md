| challenge name | haveibeenpwned |
| -------- | ------- |
| Category | OSINT |
| CTF | WISCME 22 |
| solves | 2 |
| key concepts | Socmint , osint process  |
| description | Some Important Documents have been stolen From our Office ! , we have gathered all Cards used that day. can you investigate the incident and find what really happened ?  |
| give Files | [cards.zip](https://github.com/HussienMisbah/OSINT1337/blob/master/Challenges%20Files/cards.zip) |


## Discovery

We are given a cards.zip to start our investigations with

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/5277ff52-fb38-4d0c-9ef6-248dae0ee7ca)


Each card contains the name, QR code, and Title. We can start investigating the QR-Codes first. Using any online tool you can get the Data of Qr-codes


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/0bdd81c7-82d8-4299-a20e-5c7d70635250)

There are 2 users who have the same QR-Code data which is suspicious. Maybe someone cloned the card of the other? We don't know for sure. But we have suspects to start with.

Searching for Freda on Twitter will get the account

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/071beaa7-84c9-4d64-b1e9-da40726b1b9b)

We can see these tweets

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/4a2d1ecb-def2-4903-8708-7c3ec2e7ca06)

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/6d48fc2c-d5a7-455c-8a53-6b2c0d0ec12d)

It seems she got hacked recently and we can see this tweet which contains a link, we can type it easily it is not a fully blurred file.fm/f/t2yvg6anj


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/19dc624b-b47a-4b14-a4cc-29ba8d78a199)


From the context, we can know this is the emails between her and the attacker who encrypted her files

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/72379a59-0530-4281-8f02-7c5a625f909a)

Downloading the emails , we can view it with any online service 


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/eb843198-576c-4540-b8e1-41b94ccd1651)


- Keep reading the emails we can understand someone tricked her by telling them he hacked her and she needed to click a link then a malicious file would be downloaded which causes the files to be encrypted

- Here we can see she sent him an encrypted file to decrypt it as a POC he can do so.

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/25f181f5-d0cb-4fde-9d59-38ae83f91141)


The link has this file


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/6c05728b-a4fb-4774-be8e-d2579b75814d)


- The next mail contains the decrypted file but seems the link is down, so we can try to decrypt it ourselves. We don’t know the ransomware name.
- We can search by the img we have found on Twitter and will know it is jigsaw ransomware

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/a5936601-493c-40b3-9499-28e85376f8bd)


Searching online on how to decrypt it will find this github script


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/a34db610-7f39-40ee-a17e-a070d00eb84b)


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/c76924d4-1049-485c-b703-4d6a59557ecd)

And now we can get the first part of the flag


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/3bf8c2d8-1ea4-41a1-b521-9a666a1db95f)


- Now this mail kept showing up in the mails and the image we can try to search

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/c76c309a-2653-46b5-b116-167b1c531aff)


Using Epieos we can get his First and Last name


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/021a046f-2b20-4037-b808-f89eb820dfd4)

Searching for him on Twitter

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/d8335119-2832-408b-bf04-9ed71800d844)


We don’t see any tweets but we can see the name CT_APT1337 , Looks like it is APT Group. And where do APT Groups lives these days?- on telegram

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/679dd063-193e-43f8-a1cb-a190854ed2c5)


Downloading it we can get the 2nd part of the flag


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/9c2ad15d-29ce-4dd1-bfbf-6fe8eac638f9)

