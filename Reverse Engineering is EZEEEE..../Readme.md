

We have been provided with a windows executable file named examine.exe. Executing it, starts a snake game as below

![Screenshot (114)](https://user-images.githubusercontent.com/111695465/210226409-46e5b165-ab25-454d-8e2c-c0283b33a93d.png)

From the image, we can see the mention of pygame. PyGame is a module of python programming language. So we can assume the exe has been coded in Python.
We can assume the flag could be hidden in the source code so we have to decompile the exe file.

We can find few decompilers for python executables like decompile3, uncomplyle6, etc. 
Python has one such module named pydumpck which can be used to decompile an exe file derived from python file.

After installing pydumpck, entering the command as "pydumpck location/of/the/exe/file" as follows

![Screenshot (115)](https://user-images.githubusercontent.com/111695465/210228689-fdddbe1f-5f11-422f-bea0-b5fa81e40353.png)

This creates a folder with various files one such file is the examine.
