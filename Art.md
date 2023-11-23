| challenge name | Art |
| -------- | ------- |
| Category | OSINT |
| CTF | Arab Regional Finals 2022 |
| key concepts | osint process  |
| description | we have received news that there are some criminals planning to steal something valuable and our friends were able to get us some emails between the criminals but we didn't figure out their plan yet. can you help us? |
| Given Files | [mails.eml](https://github.com/HussienMisbah/OSINT1337/blob/master/Challenges%20Files/mails.eml) |


we have a .eml file attached which we can inspect , we can open it using any text editor , Iwill use notepad++

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/f588a4a7-f354-44e8-b5fd-78265bc74a89)

We can see some headers for the mails sent and a huge base64 encoded text which we can decode at cyberchef


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/b78f3742-93b1-4282-b345-6202be3b740a)


We can take the decoded text and start analyzing it :


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/b1d1bfaf-79a2-490e-83c9-fc1dca56deca)


We can see the second message when muner responded to rashiid telling : 

*send me details in Our old method in case these emails went in the wrong hands!*

And then rashiid send a huge essay which seems irrelevant to the operation they are talking about


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/51c5c700-65ba-4441-9b6e-1918cd3a9c97)


For the purpose of formatting the text so we can read it , we can replace :

``.`` -> ``.\n``


If we look at the text now we can see a character is added at the start of some lines which makes meaningless words like during -> rduring the “r” is appended


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/7b06e413-2816-4122-a278-0f52fec879dd)


Extracing all suspicious character we will get : ``r2q6f3n8k``


It is totally meaningless (for now) , so we can keep investigating until we find new information in the text.


If we look closely at the huge text we can notice some words has Upper case in a suspicious place like paciFied. Maybe this is the cipher they are speaking with ? We can write a small python script to extract all upper case letters

```python
for i in text:
  if i.isupper():
    print(i)
```

Running it we get : ``FILEFM``

We can start searching for FILEFM and we get it is a platform for sharing so r2q6f3n8k should be the ID of the share


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/541f735f-ee38-4416-b5de-27964fe642e4)


We can upload anything to know the structure of the link and we got

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/7931999d-9aea-4889-a94d-8e7c2d499162)


So the link rashiid want to send to muner is: https://file.fm/u/r2q6f3n8k , we can visit it now and we will get diagrams for the place of the operation


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/baf60c87-eef2-4f2c-a011-e2135d2fd08b)

but we got no flags , checking the author of the uploaded files , will see a link icon to a github page 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/fdfe408d-e8cf-4f85-8477-4c0723166719)

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/d78601c7-77a7-4f6a-8382-dd87bdab260d)


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/0a75e316-4869-4e1b-8ea2-110606339a16)

- and finally will see this commented image , flag at meta data headers 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/75a1d722-7e1a-44f3-87f9-04ff8b265e8f)





