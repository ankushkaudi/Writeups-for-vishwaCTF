Writeup for Locks n Keys

Given files : Johnny.zip

We have been given a .zip file.
Extracting the .zip file asks for the password which is not given. We can think of cracking the .zip using some tools.
One such tool is John The Ripper. Cracking the .zip using John gives the password as “thunderbird”.
After extracting, 11 image files named zero,one,….,nine, justanimage and a text file. Renaming the files with numbers instead of text as 0,1,…,9 we can see combining it gives some message. There are 3 messages we can extract from it as
1.	256*1024
2.	itisjustastring
3.	Do you know what is the extension of an encoded file????  
4. 41 45 53 02  
The text file says "Sometimes, what you see isn't what you get." Using file command on justanimage.png doesn't give much about info abou png file. From the text file, we can assume the given image might not be a png file but something different. From the line 4 we can use the data to change the first four hex values of the png file in hexeditior and renaming it to the file with extension .enc (as line 3 says about an encoded file)

![Screenshot_2023-01-22_13-49-21](https://user-images.githubusercontent.com/111695465/213907503-51a292d4-da10-4cc5-a3ea-44e3ef460e49.png)

From the first line we can see “created by pyAesCrypt”, we can assume this file has been encrypted with pyAesCrypt of python which is an AES encryption module.
We can encrypt and decrypt with the in-built functions of this module.

![image](https://user-images.githubusercontent.com/111695465/213907524-e58dbe9e-bdab-49df-932b-4d9c7721eac3.png)

From the above code, line 1 is used to encrypt a file and line 2 is used to decrypt a file with a password.
The password and buffersize has been provided.
After decryption, the below image appears which is an inverted qr code

![main](https://user-images.githubusercontent.com/111695465/213907533-2c4bbbc9-e004-4ea6-bc90-183e85cc700e.png)

We can invert the colours and obtain the original qr code

![qr flag](https://user-images.githubusercontent.com/111695465/213907544-9693e3e1-15b5-48bd-b62d-ee5a8ceb57ee.jpg)

Scanning above qr code will give the flag
Flag : vishwaCTF{3ncrypt!0ns_4r3_b0r!ng!!!!}
