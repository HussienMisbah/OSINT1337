| challenge name | D1rk |
| -------- | ------- |
| Category | OSINT |
| CTF | Africa Regional 2022 |
| key concepts | osint process , onion links |
| description | We are gathering some information about some guy can you help us? , we know that he has the Username Zayaya on one of the oldest link directories on the dark web, Famous for listing all important .onion links. Visit the original page and get us the information of the email address of this guy Flag in format flag{guy-mail@example.com} |

First we need to find what page the description is talking about. I Will search google for: 

"one of the oldest link directories on the dark web. Famous for listing all important .onion links"

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/cd431b36-de08-4670-a9e8-1674d4841305)

All results are pointing to what is called “The hidden wiki” 

So we need to search about this “the hidden wiki” to obtain any information that can assist us 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/481ccf8d-018e-42c0-8a8a-1d989dd8c9ab)


Visting this page we will see a lot of onion links:

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/a371ec6c-86f5-491d-80e7-653549ac50b4)


There is alot of onion link for “The Hidden Wiki” so which one to visit, if we get back to the description will see “original” so it means we need to check “the original hidden wiki” 

We have this onion link:

http://zqktlwiuavvvqqt4ybvgvi7tyo4hjl5xgfuvpdf6otjiycgwqbym2qad.onion/wiki/index.php/Main_Page


We can’t access onion link from chrome or usual browsers, we need tor browser. 

Install it using:

```bash
 sudo apt install -y tor torbrowser-launcher
```
Then choose whatever configurations you need, and visit the link we have:

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/f9f29891-5e05-4197-89e4-f43882ea9e2a)

The Description also mentioned something about information, so on the left side we can visit the page information 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/e9c4b39d-c650-40ce-9612-d6c3102e2604)


If we try to go to the Admin2 Profile , we can know the username convention is written as 

``http://zqktlwiuavvvqqt4ybvgvi7tyo4hjl5xgfuvpdf6otjiycgwqbym2qad.onion/wiki/User:Admin2``

So we can change the Admin2 to Zayaya to get the email address

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/49d80fe3-620c-4dee-a375-e64a57aeecb4)
