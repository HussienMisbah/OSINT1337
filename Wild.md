| challenge name | Wild |
| -------- | ------- |
| Category | OSINT |
| CTF | CyCTF Quals 2023 |
| key concepts | reverse image searching , Socmint , osint process |
| description | Based on the image given , can you show your exceptional open source intelligence skills to get the name of the man in the given image , format example:CyCtf{Mark_Test}|
| Given Files | [wild.jpg](https://github.com/HussienMisbah/OSINT1337/blob/master/Challenges%20Files/wild_medium.jpg) |


The given image shows the man standing beside some planets everywhere indicating he is in a planthouse or  something like that.

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/ea005f56-055e-4320-b126-532e7f21b8e7)


Reverse image searching will lead nowhere , focusing on the plant part only return some information , it will show the plant name is ``Anigozanthos Gold Velvet`` 

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/f3150680-b6b4-453c-97fb-eb31a2958d71)


searching by plant name in google will find the video where the given image is taken from 


![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/2073c67b-09d0-4d45-b53b-7616d1ce83be)


the information we got is the man is working at ``ozbreed.com.au`` , searching for the company name we got Linkedin result shows employees names where we will find the man

![image](https://github.com/HussienMisbah/OSINT1337/assets/67979878/c56216ea-44a4-45ea-8458-adf3779795d4)


*it turned out pimeyes website was able to get information about tha man from the challenge given image and that is how it was solved by most of the teams during the Quals 😢*
