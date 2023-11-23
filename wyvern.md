| challenge name | wyvern |
| -------- | ------- |
| Category | OSINT |
| CTF | Confidential |
| key concepts | osint process |
| description | i am near you, i am with you when you need me text me and i will Be there for yOu waving wiTh a flag! |
| Given Files | none |


The Uppercase letters seem suspicious we can extract them to get the word BOT, but what BOT? 

- Checking the challenge name and checking if it makes sense, we got it is related to discord

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/6c79e511-ceec-446b-b803-a523be243ee3)

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/632a6a7b-dbdc-4d6d-bce2-acd3cd2551d4)

The Description says “when you need me text me and I will Be there for you” so trying to DM the bot

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/5797915d-0209-4f6e-8e02-4208f27d034b)

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/5ba02b77-50e3-4a95-90fd-634790d87a93)

It will give us the flag if we know the secret we don’t know for now. But we got a username. We can start from there

We got a username so we can sherlock on it to see some low-hanging fruits , it will reveal his Pastebin account 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/6dfe0ebe-0ef3-45d4-af1b-768f02d8640f)

The Urgent paste is protected with a password However we can see the paste of Hint key which is now_you_can_unlock_the_hint

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/8e8eb7c4-c1ea-414b-a51e-aa965e41a93f)

The bird emoji is a great hint for checking twitter , sherlock doesn’t reveal twitter account but we can do that ourselves , we can find his account and the profile matches the one on discord 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/9d3ea274-a3ce-4971-864e-e3fd04b89642)

We can check the tweets which have suspicious pattern at the end something like index:char

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/63a029dd-9068-46fb-9a53-b8f50a6fe26d)

Assembling the pieces will get the string V1xYsDLUMk, which worked for the Paste of Urgent in the Pastebin


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/1b17e8e0-f555-42e2-98d7-bef833a0797d)


We can take this string of Ees and try to decode it on Cyberchef , use decoded text to get your flag 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/1c94e5f1-c8d2-4ec5-b1b0-30984585a46a)
