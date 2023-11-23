| challenge name | As1at1c  |
| -------- | ------- |
| Category | OSINT |
| CTF | Africa Regional Finals 2022 |
| Solves | 9 |
| key concepts | osint process , image analysis  |
| description | your favourite osint challenge , flag is in format : flag{Latitude,Longitude} , only 4 digits after the decimal point. (ex: 112.12345 --> 112.1234)|
| Given Files | [As1at1c.png](https://github.com/HussienMisbah/OSINT1337/blob/master/Challenges%20Files/As1at1c.png) |


We are given just this image and the flag is the coordinates of this place.

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/e3a3115d-5e47-4f0b-9d83-599eb047a5e7)

We can see from the photo some kind of flag 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/ab860707-a5d0-4846-be9f-a2cb9a0f6b04)


From the challenge name, we can suspect it is in Asia. checking Asia countries flags we should see the country is Thailand

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/c465d8a6-cbb7-47d6-90de-e3611ded59b8)


So we know the country, we can check other elements in the image like the bridge shape over there.

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/7807d4c0-0bda-4c3a-b292-d3334fdb41ab)

We can suspect existing of a river 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/cc46dc69-7351-477d-92f2-8c85283101cd)

Searching for Bridges in Thailand we can find those ones , and looks like we have a similar bridge 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/3b0d91fa-cd37-4369-b3af-f8250266b9c0)

Searching for this bridge we can find it on google maps

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/993b9610-a95f-4d78-a373-c388a0622c68)

The last step to reach the exact location is to re-position our perspective down the bridge.

If we set the street view perspective in the street we can see this view , if we focus we will see the same king frame down the street


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/018535cc-7094-4602-9e78-8953e1aa0dc0)

Moving forward we will see exact same image 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/c3b87ac6-7598-4524-9dff-5fba82e93fda)
