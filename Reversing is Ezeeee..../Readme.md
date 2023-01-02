We have been provided with a windows executable file named examine.exe. Executing it, starts a snake game as shown below

![Screenshot (114)](https://user-images.githubusercontent.com/111695465/210232516-d40d44d9-e47a-48b7-96ec-357fd0930212.png)

From the image, we can see the mention of pygame. PyGame is a module of python programming language. So we can assume the exe has been coded in Python. We can assume the flag could be hidden in the source code so we have to decompile the exe file.

We can find few decompilers for python executables like decompile3, uncomplyle6, etc. Python has one such module named pydumpck which can be used to decompile an exe file derived from python file.

After installing pydumpck, entering the command as "pydumpck location/of/the/exe/file" as follows

![Screenshot (115)](https://user-images.githubusercontent.com/111695465/210232531-e657c11c-a887-4f3d-abef-8258e02d996a.png)

This creates a folder with various files one such file is the examine.pyc.cdc. We can see the source code of the exe file here.

Examining the complete code we can see a function named solution which is not at all related to the game and we can see the function makes some conversion and stores the result in the string 'out'

![Screenshot (116)](https://user-images.githubusercontent.com/111695465/210232545-a049cdb6-632a-4f92-a5e4-693e841ed320.png)


![Screenshot (118)](https://user-images.githubusercontent.com/111695465/210232566-33d87adc-20c8-489d-98c7-f2b8e602a162.png)

