
| challenge name | Revenge |
| -------- | ------- |
| CTF | CyCTF Finals 2023 |
| Solves | 1 |
| key concepts | OSINT Process  , SOCMINT (facebook , twitter , instagram , threads) , GEOINT |
| description | we think we are against bunch of related cases , we suspect the same criminal is responsible for them all but we can't find a pattern/lead to proof that. we have run out of ideas for now so your help is needed , will you do or will you just run out of time ?  - Detective 0xM
| given files  | [case719_intial_report.pdf](https://github.com/HussienMisbah/OSINT1337/blob/master/Challenges%20Files/case719_intial_report.pdf) |

## 1) Report Analysis 

- we are give a pdf file contain 4 disappearance cases , from description the detective suspects the crimes are related and it is the same criminal 
- we have 4 missed kids and reading the report here are the extracted data 

**David**

- last time seen at ``34.7011385, -92.4116201`` , he was kidnapped from house 

**Jenny** 

- last time seen at ``34.7383036, -92.2869382`` , her mother name ``Margot Garfield`` 
- found a paper in her neighbor ``Marqous dominik`` trash bin saying ``you will be missed jenny`` 


**Darline**

- one of her friends describe the criminal to have dark hair and tatto near his face
- her mother name is ``(Jessica Gibbs)`` 

**Jack**

- little kid , a car crashed his mother's car to take the kid while she lost conscious 
- house near ``34.7481701, -92.3109754`` 


## 2) Investigation Methodology 


#### 2.1) Case #1 Solution

- It will be a smart thing to try get social media accounts of little kids whom ages between 1 year and 5 years old , so it is better to focus on adults accounts 
- also note that given location are not far from each other , all in same city ``Little Rock, Arkansas, USA``

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/42d461e2-59be-4464-a2b0-fb77daac1b89)

- starting with the name `Marqous dominik` we can start searching for him in social media , however the tip here we know where he lives so we can limit our search area by using filters

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/2130490b-3ed6-4611-8829-c4822a6491f3)


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/8c6557b2-3bc9-49d1-ac64-9a8c3cf50d67)


- will find in family member his sister in law account 


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/327e1e10-8c6c-4e32-8745-cdf47f959ce3)

- in her about we can find some information we can utilize like her nickname ( we will see this information only from Facebook Desktop and not from Facebook mobile app )

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/92ffa43b-57ae-4b70-8df4-9827d88dca88)


- running anytool on the username will get her twitter account with those 2 tweets

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/15b82034-a17e-43d0-ae57-48a673b5c361)

- got a reply on someone with a link of a reddit community 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/513fe87f-5ea1-4076-8fc5-59f8a2c860e0)


- Checking the community's posts will see one from her

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/7b43b38b-7387-4db3-8d9d-7537d6f9ed70)


- and we can some sort of deal between her and the online criminal , they wanna frame her brother by giving him a lesson to leave the neighborhood 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/a62ffc65-9c48-4eb5-8507-4f940dda4978)


- we got 2 usernames from this reddit community + we can get the community author if we are loggged in and by checking the about page 

```
JasonMilmao
TianaUnderCover
JasonCyrus1337
```
- running any SOCMINT tool on first one will get his pastebin account , there is a paste for the flag but needs a password

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/fef0dc10-3e73-4726-ad22-0101b86c7236)


- we can get the password from ``JasonCyrus1337`` reddit bio 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/e79e7094-e703-4070-91b1-e0b06c89f702)


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/452334f6-8913-42a1-9920-10b253b3d471)



*So we got the conclusion this case is sperate from the other 3 cases , also note that Jenny is older than all the other kids and the only case where there was a signature by the criminal , if this was a series of connected crimes we should found some evidence for the other cases as well !*


#### 2.2) Case #2 Solution


- searching by ``Jessica Gibbs`` we can grap her facebook account easily along with her insta account 


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/bc589f1a-64af-4758-b721-64264939bcd1)

- her insta account has a post for her kid along with an email address 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/af3e6c39-f4b1-44ca-b419-a446950928ad)


- the tagged images we can find 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/30949246-3c21-4154-807b-a9e084e6a807)


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/048b8791-8f56-4311-808b-8aad4b0db224)

- The only mad kid is Jacob , and there is some thing dark near his face looks like a ``scar`` , the point here is to link that his brother name is ``Jacob Marionly`` and known as big j which means ``J`` , we can try some combinations for a username we can search with to be ``JMarionly`` 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/6410bf38-b816-4b31-911c-b2a2aa8252b2)


- we will find his twitter account and a pastebin account , the man is same as described has a tattoo near his face and has a dark long hair !

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/cd3e3b92-8df3-4efc-bd86-a41120980e91)


- Looks like we got him finally  
-  Conclusion : *the victims parents was the reason he had a scar in his face , he decided to do the same for their children to suffer same pain*

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/78004d57-fb97-45a3-9fba-4059ad59a10d)

- The pastebin needs a password to enter which we don't know , reading the tweets will find out a new person

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/a2c1c50f-bf33-4467-b0b0-4754c7fc7a93)



- the new app ``@`` is a hint for threads application , the app is quite new and SOCMINT tools has not listed it there yet

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/89e978f8-02f3-4d6b-8de0-302d5e8d3d2d)

- searching for Threads OSINT will find 2 Tips one including requesting data using graph and other for getting the full image size (not circle cropped case of avatar template)

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/f66c1492-e5f8-4cc6-a1ba-e0b363d62355)


- will get the password for the pastebin 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/74bd00a1-f887-48e9-bf2e-96d19afdb96f)

