

We have been provided with a windows executable file named examine.exe. Executing it, starts a snake game as below

![Screenshot (114)](https://user-images.githubusercontent.com/111695465/210226409-46e5b165-ab25-454d-8e2c-c0283b33a93d.png)

From the image, we can see the mention of pygame. PyGame is a module of python programming language. So we can assume the exe has been coded in Python.
We can assume the flag could be hidden in the source code so we have to decompile the exe file.

We can find few decompilers for python executables like decompile3, uncomplyle6, etc. 
Python has one such module named pydumpck which can be used to decompile an exe file derived from python file.

After installing pydumpck, entering the command as "pydumpck location/of/the/exe/file" as follows

![Screenshot (115)](https://user-images.githubusercontent.com/111695465/210228689-fdddbe1f-5f11-422f-bea0-b5fa81e40353.png)

This creates a folder with various files one such file is the examine.pyc.cdc.
We can see the source code of the exe file here.

Examining the complete code we can see a function named solution which is not at all related to the game and we can see the function makes some conversion and stores the result in the string 'out'


![Screenshot (116)](https://user-images.githubusercontent.com/111695465/210231807-cc65dbc7-d8bb-4321-8b80-5801715681e5.png)

Copying the code into another python file and printing the value of out gives the flag

![Screenshot (118)](https://user-images.githubusercontent.com/111695465/210232051-b961ac88-bc7a-4656-b33d-f6462dcb560a.png)

Flag is : vishwaCTF{!5_pyth0n_th3_b35t_l4ngu4g3????}
