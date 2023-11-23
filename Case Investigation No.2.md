| challenge name | Case Investigation No.2 |
| -------- | ------- |
| Category | OSINT |
| CTF | CyCTF Finals 2023 |
| Solves | 4 |
| key concepts | osint process  , understanding google maps |
| description | The International Criminal Police Organization has been tracking a serious criminal who wants to eliminate the mankind , they have collected his recent visited locations , can you track down the criminal ? 
||note : be smart enough and don't waste your time trying to bruteforce the zip file ;) |
|give files  | [challenge.zip](https://github.com/HussienMisbah/OSINT1337/blob/master/Challenges%20Files/Challenge.zip)|

- Based on the hint given during the CTF , your starting point is the CSV Files , the given data.csv contains the following data 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/13240ab9-dc31-4a7a-bb3b-e73963b3ff58)


- trying to search for some of them we got the following weird locations 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/78c90d57-1485-43dc-8ed4-b76d274319d6)


- the key concept of the challenge is to make use of your custom google maps option which can be found at 
```
https://www.google.com/maps/d/home?hl=en&hl=en
```

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/0f6ba6e3-9d41-42b6-a35b-24dcea590371)


- will choose create a new map , import the CSV File choose first option

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/9994c13c-ce88-4d07-b162-39c80358f500)


- once done we got the following locations 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/cf2a3fec-eba9-452b-b3b3-eabc66e37f05)


- zooming enough into some of the markers , we can see human readable text ``ARe_We_`` 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/af66252b-b696-4b42-ab26-8c795a396713)


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/78c292b7-a990-4a57-bd0e-097bc24bf0c3)


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/d34f41ea-aa19-4cb5-a2e7-25df915bc24b)


- so we got the sentence ``ARe_We_The_ReASoN_?`` which can be used to open the zipped file given 


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/202e492c-3efd-4cf2-bb2c-a3880f51f20a)


