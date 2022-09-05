### Exercises with Scanner and Files

## Task 1: Scanner basics
1.a: Start a new project and create a Main class with a main method.

1.b: In the main method start by printing a message to the user: "Please type your name".

1.c: Instantiate (create) a Scanner object for reading the command line (remember to import the Scanner class from the util library: <code>import java.util.Scanner;) </code>

1.d: Declare a String variable, <code>name</code> and assign the content of the scanner to it.

1.e: Print the value the user writes (print the <code>name</code> variable)

1.f: Print another message to the user: "Please type your age"

1.g: Declare another variable of type int, <code>age</code> and assign the content of the scanner to it (you may reuse the Scanner object created in 1.c).

1.h: Print the value the user writes (print the <code>age</code> variable)

1.i: Declare a third variable of type int. To this variable, assign the calculated number of years until the user can retire. You may assume retirement starts at 67 years. Print the result


## Task 2: Finish the GuessANumber class
2.a Open the java file above called GuessANumber.java and try to finish the code. Follow the steps written as comments in the <code>makeAGuess</code> method.


## Task 3. Textbased menu
3.a In a new project create an entity class, Menu and a client class, Main with a main method.

3.b In the main method create an ArrayList of type String called 'options' with the following values:
<li>"1. Start game"</li>
<li>"2. Resume game"</li>
<li>"3. Pause game"</li>
<li>"4. End game"</li>

3.c Still in the main method, instantiate the Menu class passing the 'options' reference as an argument to the constructor.

3.d Add a constructor to the Menu class that matches the instantiation made in 3.c. The Menu class must have a private attribute of the same type as the parameter passed in the constructor. Assign the passed options ArrayList to the private options ArrayList 
<details>
  <summary>Hint</summary>
  <p>this.options = options</p>
</details>

3.e Create a method in the Menu class, <code>showMenu</code> that prints the sentence "Choose an options by typing the number associated" followed by each individual option on its own line. (Hint: use a for-each loop). 
 
 >3.e.1 The method should return a value of type int, with the user's choice. 
 <details>
  <summary>Hint</summary>
  <p>int choice = scanner.nextInt()</p>
</details>
This should only happen if the choice is valid.
 
 >3.e.2 Additionally the method should print a message to the user if the choice is invalid (ie. greater than the number of options). 
 
 >3.e.3 In the main method call the showMenu method on the Menu instance, saving the return value (the user response) in a variable. Pass this variable as you call another method in the Main class, <code>doAction</code>, which you will write next.


3.f Create a method, <code>doAction</code> in the Main class, that accepts a value of type int as argument. This value represents the user choice of option. In the body of the method write a switch-case where:
<li>case 1 will print "Starting the game now"</li>
<li>case 2 will print "Fetching previously saved game data"</li>
<li>case 3 will print "Game paused"</li>
<li>case 4 will print "Ending game"</li>



## Task 4: load options
 
4.a Start a new textfile with the exact text given here:
"Expresso", "Americano" , "Macchiato", "Flat White",  "Latte"
Save it as a menu.csv file and placed it in the same folder as Cafe.java

4.b Create a class called Cafe with a main method. In the global scope of this class add an ArrayList of type String called 'menu'.

4.c Add a method  <code>loadMenuData</code> to the class with the parameter 'filename' of type String. 
  Have the method load the file, add it to a Scanner object.

4.d Use the split method to convert the data into a String array.\
<details>
  <summary>Hint</summary>
  <p>scanner.nextLine().split())</p>
</detail>
  This will return a String array. Loop over the returned String Array and for each element create a new String with the value of the element preceeded by an number: For the element "Expresso" there will be a new String with the value "1. Expresso". 
  Then add the new String to the menu ArrayList which you created in step 4.b

4.d Reuse the Menu class from Task 3. (copy it into the folder of the Cafe.java). Create a new instance of the Menu class, with the <code>menu</code> ArrayList as argument. Call the <code>showMenu</code> method on the Menu object. Remember the method will return the user's choice? Print the name of the coffee that corresponds to the user's choice. 


## Task 5: write to file
[...]
