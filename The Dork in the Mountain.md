| challenge name | The dork in the Mountain |
| -------- | ------- |
| Category | OSINT |
| key concepts | osint process  , dorking , website analysis |
| description | My Friend works in a Lodge , they have cameras for real time monitoring however he is not an IT Guy so he made a mistake which resulted in exposing some information. Can you answer the following Questions based on the image given ? |
| Questions | 1- What is the camera model name? (all lowercase) 2- what is the the name of my friend (note: he is the user configuring the cameras) 3- camera 1 ip address  |
| Given Files | [DITM.png](https://github.com/HussienMisbah/OSINT1337/blob/master/Challenges%20Files/challenge_DITM.jpg) |

Given the following image , the name Maliba stands out also in the description it is mentioned that it is a Lodge

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/6aac9ae4-f296-4ef4-9f8b-fce8f87489cd)

Searching for it we can find the following result

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/5ec069d8-4d6d-489d-9aa4-7a71256f0477)


Checking the website and going through different tabs , we can find the following 

About > webcams , or search by the work “cam” 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/588c6f58-84c7-4712-99b0-7e1ec0f5b111)


Visiting the page we can find 


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/aa55db3d-6778-4f8f-b331-67279a458a31)


We can see the same place the challenge image is here , so we are on the right direction , now how we can get the answers for the challenge 


Searching for the google dorks related to web cams in GHDB 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/71b5590d-707b-4d45-a1c5-28d41909d677)

``intitle:"Index of /webcam/" inurl:maliba-lodge.com``


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/12bea165-cdd5-4b14-ad51-7438946c7e4f)

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/cdcb7cf3-5351-46f2-8d1f-0cbf821928f5)


The readme file seems promising ``https://maliba-lodge.com/webcam/Readme.txt``

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/ccc9840f-46ff-4a37-86ff-24aef6e40a40)


Okay that reveals the username malibalo and the camera model is hikvision . for the 3rd part (ip) we didn’t get it but we get some hint about it. 

*The image is named with camera ip adress , date and time stamp. That is renamed by above script and uploaded to main webcam folder as cam_1.jpg*

Keep checking the cam_1 directory waiting for the image to reveal the camera IP as mentioned , note that it may take up to 15 mins as the image are taken every 15 mins.

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/c5d950cd-2a16-4dc3-a9a4-8c0efa18ebb5)

