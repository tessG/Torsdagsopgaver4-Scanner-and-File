# cph-1st-w39


Task 1-4 træner base class operations og skrivning af klasser i "ren" Java. De skal kodes i en almindelig text editor uden Processing. Task 5 og 6 er i Processing miljøet.


Såfremt I sidder fast ved en opgave, så tag en kort pause og prøv igen. Hvis I stadig sidder fast ved den, så hop videre til den næste.
Generelt er det bedre at I får tænkt over alle opgaverne, end at I får løst dem allesammen fuldkommen. 
Endvidere er I meget velkommen til at tale sammen om opgaverne, men det forventes at I alle koder hver jeres løsning. 


Opgaverne skal ligesom sidste uge, afleveres på moodle, via et link til jeres github repo. 


## Task 1. Palindrome
  1.a Skriv en metode printIfPalindrome() som tager en tekststreng som argument og printer den HVIS den kan skrives bagfra uden at ændre sig. (Hint: Lad dig inspirere i dokumentationen for String klassen)
  1.b Sørg for at metoden ikke er case-sensitiv.
  1.c Kald metoden fra main med argumentet "Den laks skal ned", for at teste den.

## Task 2. print en delmængde af et ord med fejlhåndtering
I denne opgave skal du brug substring metoden, og du skal fange StringIndexOutOfBounds exeption som Java vil smide i tilfælde hvor metoden bliver kaldt med for høje tal.
2.a Lav en metode, printPartOfWord(), med tre parametre: 1. parameter er ordet, 2. parameter er index for det bogstav delmængden starter med og 3.  parameter er længden på delmængden
Ex: argumenterne "København", 1 og 4  skal give outputtet "øben". 
2.b Sørg for at metoden kan håndtere at blive kaldt med tal-argumenter som er for høje eller for lave. Brug en try catch hvor du håndterer undtagelsen StringIndexOutOfBounds. Du bestemmer selv om der skal komme en besked eller ske en udskiftning af det fejlagtige tal-argument.


## Task 3 (ArrayList)
3.a In main Create an array called cars, of type String with 3 car brands in it.
3.b import java.util.Arrays 
3.c Create a method that takes a String key as argument and uses this as the key argument in the binarySearch method(Arrays.binarySearch(cars, key)). Note that the array must be sorted before using binarySearch
3.d let the method return the return value of the binarySearch call and print it from the main method

## Task 4 (Math and Random):
4.a Create a class MathWork add a main method.
4.b Write a method 'divisible', that takes in an integer as a parameter and prints all values between 0 and 100 that are divisible by the parameter received. 
    (hint: you need to use the % operator)
4.c call the method from main 
4.d add the following array to the class: int[] arr = { 1, 1, 1, 2, 2, 3, 3, 3, 4, 5, 5, 5, 6, 6, 7, 8, 8, 9, 9, 10 }
4.e Write a method, 'getRandom' that returns a random element from the above array.
4.d Write a function that takes an integer as a parameter and prints the number. After that, it subtracts one from the input and calls itself again (recursion). If the input is less than zero, it should no longer call itself. 
4.e Write a method, fibunacci that takes two integers as parameters and prints the first of them.
 Each printed value should followed by a tab ( \\t ). Then have the function calculate and print the fibunacci sequence (0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144) by calling itself. If the input is greater than 1000, then stop. Start the function by calling it from main with the input (1, 1).
(hint: how to calculate the fibunacci sequence: https://en.wikipedia.org/wiki/Fibonacci_number )

## Task 5 (Debugging):
In the directory above named "Debugging", there are 10 different small sketches, each of which containing some kind of error. For each of the sketches, try to run it firstly, then have a look at the output and afterwards fix the error. You're done with the sketch, once it prints "Job's done". 


## Task 6: Draw a chess board using a nested for loop and a double int array. 
In this task you will create an integer array with 2 dimensions, that holds values of 0, 1, 0, 1, etc. The instructions below will help you get started. 

6.a Create a double int called board[][] with the length of 8 in both arrays. 
6.b In setup() create a double for loop that loops through the board and alternates between assigning the value of 0 and 1 (e.g. board[x][y] = 0;). Hint: use the modulus operator
6.c In draw() create a double for loop that loops through the board and draws a rect for each element with the sideLength of 40 (e.g. rect(x * sideLength, y * sideLength, sideLength, sideLength); )
6.d Before drawing the rect in the previous step, add a fill() statement, that fills with the value of 0 if the board[x][y] == 0 and  255 if the the board[x][y] == 1.

# Other exercises (optional)
If you got stuck or if you finished the above, following are 3 links to exercises, where there is something for all levels.

https://codingbat.com/java 

https://www.codecademy.com/catalog/language/java 
 
https://www.hackerrank.com/domains/java 

https://edabit.com/ 

https://www.programiz.com/java-programming 
