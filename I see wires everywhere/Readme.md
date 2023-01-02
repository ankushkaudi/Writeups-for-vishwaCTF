We have been provided with two files a_hint_for_you.jpg and lissen_carefully.wav. Trying to extract hiiden files from these using steghide,, it asks for passwords.
From the description, we can see the first two names are written different. Trying massimobanzi as password for lissen_carefully.wav and davidmellis for a_hint_for_you.jpg, files get extracted as shown below.

![Screenshot_2023-01-02_23_37_49](https://user-images.githubusercontent.com/111695465/210266885-4e006527-0001-4890-ad5d-7911c641eaa4.png)

We can see code.ino.hex and info.txt files appeared. info.txt has the following data

![Screenshot_2023-01-02_23_45_05](https://user-images.githubusercontent.com/111695465/210266957-84d62543-bf82-487f-a10d-fc113c626b7d.png)

This text files tells about the electronic components and their quantity. 
Reversing the audio given gives the hint of making connections. We can assume building a circuit using these components might get us the flag. Also, using Arduino in simulation requires a hex file, looking for some simulation softwares like Proteus make it possible.
According to the audio, the connections will look as follows

![Screenshot (120)](https://user-images.githubusercontent.com/111695465/210267486-3de69a67-9b3a-462d-adff-8e465922cacf.png)

Giving the obtained hex file as input to the Arduino, the circuit starts working and LCD begins to display as follows

![Screenshot (121)](https://user-images.githubusercontent.com/111695465/210267663-08a39440-9d0e-4ca5-b018-076c271b90ff.png)

But the flag is not displaying, maybe a coorect input to logic toggle may give us the flag. Looking at some other steganographic methods, we can try exiftool on the image.

![Screenshot_2023-01-02_23_57_54](https://user-images.githubusercontent.com/111695465/210267873-a30e0118-e388-4324-a8e1-e2e0e56d3b89.png)

We can see in the certificate tag, a message is written as "Grey code is 1110 enter binary", entering binary value can give us the flag
For grey code 1110, the binary will be 1011. Trying out this in the circuit gives the flag on the LCD screen.

![Screenshot (122)](https://user-images.githubusercontent.com/111695465/210268136-a644cb04-aaca-4865-a632-13b9214efba4.png)

Flag : vishwaCTF{s!mul4t3_b3f0r3_!mpl3m3nt4t!0n}

