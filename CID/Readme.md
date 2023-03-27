Description is provided in the image  
File given : case69.jpg  
Domain : Steganography  

We have been given with a jpg file case69.jpg. Using binwalk on this image file gives info that there is 7-zip file in this image.  

![image](https://user-images.githubusercontent.com/111695465/228020025-6a8801a1-5668-4d33-8687-588ad0c8a4da.png)  

The 7-zip file can be extracted using the command “7za e code69.jpg” which gives 1000 images and 1 text file.  

![image](https://user-images.githubusercontent.com/111695465/228020298-fd9a3e66-cc94-4046-b35c-3a73ddde2fa8.png)  

The text file says “You are very close mate. The flag is just around here. Hope you find it.”  
The flag might be in any of the image.  
Using exiftool gives the following  

![image](https://user-images.githubusercontent.com/111695465/228020459-2ef11c31-4bd0-4695-886f-a45410c1b3d4.png)  

We can see a PASS which is  “daya darwaza tod do” which might be a password to extract the flag.  
Steghide is one such tool which uses password to hide secret files in images. But extracting hidden file for 1000 images might be tedious.  
We can use the shell command to perform one steghide command on all the images.  
We can use shell command using “export PS1=‘$ ‘” command. A shell will get created.  
Executing below command will extract flag.txt which has the flag.  
“ls | while read line; do steghide extract -sf $line -p "daya darwaza tod do"; done”  
Using cat flag.txt will display the flag  
Flag is : vishwaCTF{my_GOD_D4ya_tumn3_t0_fl4g_dhund_liy4....}  

