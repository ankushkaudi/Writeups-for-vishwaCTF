Writeup for the challenge Treasure Hunt

The question starts with a link given as https://chic-macaron-a6bc25.netlify.app/ 
After clicking the above link, a page opens up which has a text paragraph written about treasure hunt. This page has the link to the next step of the question given as :
<Click Here to start adventure> 

![image](https://user-images.githubusercontent.com/111695465/209706564-34c91d5d-871e-4032-9475-b97e202c51e4.png)
  
After clicking the above link, a new page opens with some message as “I have no hints/clues….” and a gif is shown and also a zip file is given to download.
  
![image](https://user-images.githubusercontent.com/111695465/209706648-2ba63ffc-2399-4c9b-9eeb-8b22ba63ae09.png)
  
![image](https://user-images.githubusercontent.com/111695465/209706667-95ea3059-6451-436d-98a5-c4c756dfd3b3.png)

After extracting the zip file, a folder appears which consists of 10000 text file all of with same size and message as “Sorry bro, you’ll not find anything here. Have a nice day”
  
![image](https://user-images.githubusercontent.com/111695465/209706734-1a563b51-5c9e-4d2e-a229-bf812d7516b6.png)
![image](https://user-images.githubusercontent.com/111695465/209706745-797c2a8d-1462-471a-9426-b7a4151b27c5.png)

Moving back to the website, in the /robots.txt file there are two hints given as:
1. 6969
2. youcantseeme

![image](https://user-images.githubusercontent.com/111695465/209706873-cca1c6f2-d9f3-4c7b-aa96-6a726645afe1.png)

As we had 10,000 text files in the zip file, opening the file 6969.txt gives the hint for the next step. There is a github link gives which is as follows:
https://github.com/07anonymous404/Treasure-Hunt.git/
  
![image](https://user-images.githubusercontent.com/111695465/209706993-09501eed-2374-44b5-bfe0-02f2fa18e7de.png)

which contains three files namely,
endisbeginning.wav, endishere.exe and info.txt.

![image](https://user-images.githubusercontent.com/111695465/209707027-1ffb59cc-e9ab-4b88-80bf-07fb4f1908e8.png)

After opening the info.txt file we can see a hint given as “I got two files in here. Can you guess how it can be used to get the treasure?”
  
![image](https://user-images.githubusercontent.com/111695465/209707107-1b70928a-ab88-41fd-a923-822d6d37650d.png)

From above hint we can assume that the flag might be in any of the two given files.
Starting from the endishere.exe file, since it is an executable file it can be run only in the windows operating system and not in any other. After running it, it asks for our name after entering our name it displays some message as :
“Hey entered_name, Welcome to CTF. Hope you are enjoying finding the flag. The rules are simple just enter the password and get the flag”
and it asks for the password.
For an incorrect input of the password, it gives a message as :
“Nice try, but it didn’t do it. Please try again!” and stops after 10 sec.

![image](https://user-images.githubusercontent.com/111695465/209707161-a61fbbcc-d6af-41c0-9b41-510e9df47c3e.png)

We can assume the password for the endishere.exe file maybe hidden in the endisbeginning.wav file.
  
So looking for some steganographic tools in Kali Linux, we can find few like exiftool, steghide, etc. Trying to extract the password from the endisbeginning.wav file using steghide, a passphrase is required to extract which can be found in the robots.txt from the website. Entering the passphrase as “youcantseeme”, a jpg file with password gets extracted which is “c4ny0uf!nd!t”.                         
  
![image](https://user-images.githubusercontent.com/111695465/209707229-47c6e6dc-ee4e-4897-a6f1-1d2290e9bb99.png)

![image](https://user-images.githubusercontent.com/111695465/209707245-f5301c5a-13e8-4d43-b1c2-cc3f4722529c.png)

Entering this password in the endishere.exe file, it gives us the flag which is 
  
![image](https://user-images.githubusercontent.com/111695465/209707297-788eb7a1-4213-415e-b3e3-bb82dce759ec.png)

Flag : vishwaCTF{w3lc0m3_t0_y0ur_d4rk_s!d3} 


