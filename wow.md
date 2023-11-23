| challenge name | wow |
| -------- | ------- |
| Category | OSINT |
| CTF | Cybertalents scholarship 2022 |
| key concepts | osint process , tracking location  by BSSID |
| description | While tracking suspect activity on the internet we have found the attached information, can you help us track the suspect and find his location? The flag is in format flag{lattiude,longitude} , Use only 3 digits after the decimal point. (ex: 112.1235 --> 112.123)|
| Given Files | [screenshot_support_chat.png](https://github.com/HussienMisbah/OSINT1337/blob/master/Challenges%20Files/screenshot_support_chat.png) |


From the Description, we know that our goal is to track a user's location and we are just given a screenshot from someone and support. The only interesting piece in the chat is the BSSID


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/b9c1b197-fe7c-40e7-a31c-b2398129f0ef)


A simple google search on how to track it will find wigle.net (needs an account)


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/abe37bc6-f23f-4858-8c30-4a2a1f4861b0)

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/33f44fcc-fbde-4879-af61-15e1f30d9362)

Will see a place that has been highlighted on the map zoom into it

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/a2b20c49-0e13-4889-96f4-200150de83c1)


Watch the URL will know the coordinates:

``maplat=21.46358544507867&maplon=39.171578578521554&mapzoom=20``
