# Sorting Array Elements
## About The Project
*This is a Sorting program that Sorts the integer Values of an array that entered by the user 
and print them in either*
1. Assending Order Sort
2. Dessending Order Sort
3. In Both of them

*Using one of these three Sorting Algorithms:*
1. Insertion Sort
2. Selection Sort
3. Bubble Sort

## Tools
* Assembly Programming Language
* Visual Studio Code (Editor)
* Irvine Library
* MASM32 (Compiler)
* CMD (Excuting Code)

## Links

* [ Visual Studio Code ](https://code.visualstudio.com/Download)
* [ Irvine Library ](http://csc.csudh.edu/mmccullough/asm/help/index.html?page=source%2Fmacros32%2Fmdumpmem.htm)
* [ MASM32 assembler ](https://www.masm32.com)

## Sorting Algorithms
### 1. Insertion Sort 

*   *In This Sorting Technique of the Array Elements assuming ascending order technique we Select the first unsorted element then swapping other elements to the right to create the correct position and shift the unsorted element then we advance to select the next one and repeat this again until the whole array is sorted.*


* **_For Example :_**

![i1](https://user-images.githubusercontent.com/47761503/148007906-2e9e987e-635e-4888-8c17-b017cb5035e2.PNG)
![i2](https://user-images.githubusercontent.com/47761503/148007911-2bad673b-f755-4520-bffa-59f4e615d36f.PNG)
![i3](https://user-images.githubusercontent.com/47761503/148007913-a9ec273d-658e-4fb1-be69-5f74e7b5a2fb.PNG)
![i4](https://user-images.githubusercontent.com/47761503/148007914-641eabde-3408-42f4-8c90-3d5783cf0e8b.PNG)
![i5](https://user-images.githubusercontent.com/47761503/148007919-5a2d96c5-1d4e-4a8c-9470-f2172e88efdb.PNG)
![i6](https://user-images.githubusercontent.com/47761503/148007920-02e106eb-a4ef-4592-918e-a9fdac42a86a.PNG)
![i7](https://user-images.githubusercontent.com/47761503/148007922-084cb7a8-855a-416d-9272-7a95b1728917.PNG)
---
 <mark> *This Process is performed n-1 times where n is the Array Size until it is finally sorted* </mark>
    
![i8](https://user-images.githubusercontent.com/47761503/148007905-de837187-0d55-40ca-b745-930ac06fe01b.PNG)

*  **_Time Complexity:_**
    
     O(n<sup>2</sup>)
     
 * **C++ Code :**
 
```
// C++ Insertion Sort Code

	int arrsize = sizeof(array) / sizeof(array[0]);

	for (int i = 1; i < arrsize; i++)
	{
		int currentValue = array[i];
		int j;
		for ( j = i; j > 0 && currentValue <= array[j - 1]; j--)
		{
			array[j] = array[j - 1];
		}
		array[j] = currentValue;

```
***
### 2. Selection Sort 

*   *In This Sorting Technique of the Array Elements assuming ascending order technique we are iterating over the array elements that are unsorted to find the maximum one and swapping it at the end with last unsorted one and repeat this again until the whole array is sorted.*


* **_For Example :_**

![selectionsortnew](https://user-images.githubusercontent.com/47761503/147995391-86e05f72-c24f-4dfd-a00a-4b119f74577c.png)

*  **_Time Complexity:_**
    
     O(n<sup>2</sup>)
     
 * **C++ Code :**
 ```
// C++ Selection Sort Code

	int arrsize = sizeof(array) / sizeof(array[0]);
	for (int i = arrsize - 1; i > 0; i--)
	{
		int MaxIndex = i;
		for (int j = i - 1; j >= 0; j--)
		{
			if (array[i] > array[MaxIndex])
			{
				MaxIndex = i;
			}
		}
		swap(MaxIndex, i);
	}

```
***

### 3. Bubble Sort

*   * This is a Sorting Technique that compares two adjacent elements and swaps them until they are not in the intended order until the whole array is sorted..*


* **_For Example :_**

![bubble sort](https://user-images.githubusercontent.com/47761503/148011706-3e334a1e-9e12-4ec8-ab23-a7effd0445c9.png)


*  **_Time Complexity:_**
    
     O(n<sup>2</sup>)
     
 * **C++ Code :**
 ```
	// C++ Bubble Sort Code

		int arrsize = sizeof(array) / sizeof(array[0]);

		for (int i = 0; i < arrsize - 1; i++)
		{
			for (int j = 0; j < arrsize - i - 1; j++)
			{
				if (array[j] > array[j + 1])
				{
					int temperary = array[j];
					array[j] = array[j + 1];
					array[j + 1] = temperary;
				}
			}
		}

```
***
## Irvine Libraray
* *We have used this library to print messages to the user, and also the ineger values that he enters then checking if this entered values are valid or not.*

* ***<ins>Used Procedures:</ins>***
    1. **WriteString :**  Writes a null-terminated string to standard output that EDX register points to it and move the cursor to the beginning of the next screen line. It has no return value.
    2. **Crlf :** Writes a carriage return/linefeed sequence (0Dh,0Ah) to standard output.
    3. **ReadInt :** ReadInt - Reads a 32-bit signed decimal integer from standard input, terminated by the Enter key.

        Leading spaces are ignored, and an optional leading + or - sign is permitted.

         ReadInt will display an error message, set the Overflow flag, and reset EAX to zero if the value entered cannot be represented as a 32-bit signed integer.

         - Return args:
         
                     If OF=0, EAX = valid binary value, and SF=sign.
                     If OF=1, EAX = 0 (invalid input)
                     
    4. **Writeint:** Writes a signed 32-bit decimal number that is stored in EAX register to standard output in decimal format with a leading sign and no leading zeros.
* ***<ins>Library issue:</ins>***
<br>
         If the user have enterd nothing the input will be accepted and considers the input to be 0 and assign it to the EAX register as an input.
                

## Projeect Contributors
* [Rawan Mohammed Adelhady](https://github.com/rawanmohammed99/)
* [Salah Khalil Salah](https://github.com/SalahKhalil1/)
* [Bassim Attia Abdelatty](https://github.com/Baccem/)
* [Moaaz Anwar Elsayed](https://github.com/moaaz1010/)
* [Ziad Gamal Ahmed](https://github.com/ziiadgamal/)

