Description : Somewhere I got to know that CTF players are very good at Mathematics. Is that true?? Maybe you can answer it :)

Note : Submit the flag in the format VishwaMini{}

We have been provided with the file named coolstuff. Using file command tells us that the given file is a compiled java class. Running the java class file gives questions based on simple Mathematics and for incorrect response, the program will Exit.

![image](https://user-images.githubusercontent.com/111695465/222478833-8f936ce7-dc30-4320-a9a4-ecae5764843e.png)

For a correct response, next question is given along with two characters. We can assume that for each correct response characters will be obtained which might be the flag. 
But this might take a long time as solving the mathematics can take a lot of time. Hence, reversing the class file with Ghidra to obtain the source code might work. 
Reversing the class and examining the code in Ghidra shows there are functions each representing a question and the broken flag.

![image](https://user-images.githubusercontent.com/111695465/222479022-932a3463-8b5c-4764-88d0-8a62a463d550.png)

Analyzing the main function, we can see the order of function calls 

![image](https://user-images.githubusercontent.com/111695465/222479180-36487f52-9843-429e-9838-a8ed0e5748f6.png)

Checking the functions in the order of their call, we can extract the broken strings. Concatenating these will give the final string which is 
	e4lz3e4lauz_a5_ugggd.
This seems to be a Caesar Cipher, decrypting which gives the flag which is
	m4th3m4tics_i5_coool

Final flag : VishwaMini{m4th3m4tics_i5_coool}
