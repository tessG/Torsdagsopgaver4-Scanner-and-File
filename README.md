### Exercises with Scanner and Files
Today's tasks should be coded using the IntelliJ IDE. For each Task you will create a new project, as each task will require you to create a Main class with a main method (except for Task 2). 
In some tasks you will write all the code in this main method, while in others you will be asked to make both a Main class with a main method in it (sometimes refered to as the "client class") and an "entity class" whithout a main method but with a constructor. 

NOTE: Task 4 and 6 are not easy. Follow the steps as long as you can. Use the hints and codesnippets provided. The goal is to prepare yourself for review, where we will code it together. 

---
## Task 1:ArrayList basics
[...]

## Task 2: Scanner basics: calculate retirement age
2.a: Start a new project and create a class called Main with a main method.

2.b: In the main method start by printing a message to the user: "Please type your name".

2.c: Instantiate (create) a Scanner object for reading the command line (remember to import the Scanner class from the util library: <code>import java.util.Scanner; </code>)
<details>
  <summary>Hint</summary>
  <p>Remember that Scanner can take System.in as an argument to the constructor. System.in reads from the terminal/command prompt just as System.out prints to it.</p>
</details>

2.d: Declare a String variable, <code>name</code> and assign the content of the Scanner to it.
<details>
  <summary>Hint</summary>
  <p>You will need to use one of Scanner's methods to read the content. You can get an overview of Scanner's methods in the <a href="https://docs.oracle.com/javase/8/docs/api/">Java API</a>.</p>
</details>

2.e: Print the value the user writes (print the <code>name</code> variable).

2.f: Print another message to the user: "Please type your age"

2.g: Declare another variable of type int, <code>age</code>, and assign the content of the Scanner to it (you may reuse the Scanner object created in 2.c).
<details>
  <summary>Hint</summary>
  <p>You will need to use <i>another</i> of Scanner's methods to read the content as you are now reading an int and not a String.</p>
</details>

2.h: Print the value the user writes (print the <code>age</code> variable).

2.i: Declare a third variable of type int. You can call this <code>result</code> or whatever you want. To this variable, assign the calculated number of years until the user can retire. You may assume retirement starts at 67 years. Print the result.

---

## Task 3: Finish the GuessANumber class
3.a Open the java file above called GuessANumber.java and try to finish the code. Follow the steps written as comments in the <code>makeAGuess</code> method. Recursion is mentioned. This means that the method must call itself. If you cannot make recursion work, you can use a loop inside the method instead. 
<details>
  <summary>Not sure about recursion?</summary>
  <p><a href="https://www.geeksforgeeks.org/recursion-in-java/">Read about it here</a></p>
</details>
---

## Task 4. Textbased menu for a game
In this program the user is presented with a list of actions. When he types a number associated with an action, the program will print a response that corresponds to that action.

4.a Create an entity class, <code>Menu</code> with a private field/instanse variable, <code>options</code> of type ArrayList. 
 <details>
  <summary>Hint</summary>
  <p>Remember to import java.util.ArrayList.
  </p>
</details>
Add a constructor with a parameter of type ArrayList.  
Assign the value received, to the <code>options</code> field. 


4.b Create a client class, <code>Main</code> with a main method. 
(You will use this class to test the <code>Menu</code> class).

4.c In the main method create an ArrayList of type String. Call the ArrayList-variable <code>actions</code>. Add the following String values to the <code>actions</code> ArrayList:
+ "1) Start game"
+ "2) Resume game"
+ "3) Pause game"
+ "4) End game"

<details>
  <summary>Tip for testing:</summary>
You can test the actions ArrayList by printing one of the elements:

<code>
System.out.print(actions.get(2)) // expected output: "Pause game"
</code>
</details>

4.d Still in the main method, instantiate the Menu class with the actions reference as an argument to the constructor. 

4.e Create a method in the Menu class, <code>showMenu</code> that prints the sentence "Type a number to choose" and then prints each element in the <code>options</code> attribute. 
 <details>
  <summary>Hint</summary>
  <p>use a <code>for-each</code>loop for printing the options
  </p>
</details>

4.f Still in the <code>showMenu</code> method, create a new Scanner object. Declare a variable <code>String choice</code> and assign it the user's input. 

<details>
  <summary>Hint</summary>
  <p>
    The user input will be returned by <code>
    scanner.nextLine();
    </code>
  </p>
</details>

<details>
  <summary>Solution to this step</summary>
  <p>
    <code>
    Scanner scan = new Scanner(System.in);
    String choice = scan.nextLine();
</code>
</p>
</details>

4.g Let the <code>showMenu</code> method return the user's choice. 

4.h Create a method in the Main class, for testing that the user dialog in the Menu class works as expected. The method should have this signature: <code>public static void doAction(int action)</code>. The <code> int action </code> parameter represents the user's choice of action. 

4.i In the body of the <code>doAction</code> method, write a <code>switch-case</code> whith a case for each of the 4 actions added in step 4.b. In each case block you will print a message that corresponds to the user's choice of action:
   + 1: "Starting the game now"
   + 2: "Fetching previously saved game data"
   + 3: "Game paused"
   + 4: "Ending game"


4.j In the main method call the <code>showMenu</code> -method on the Menu instance, saving the return value (the user response) in a variable. Convert the value to an int before using it as an argument in a call to the <code>doAction</code> method in Main.


---
## Task 5: load file and write to file basics
[...]

---

## Task 6: load coffee menu for a cafe
In this program we will load a list of coffee names and display it to the user. We will create a Cafe class that loads the list and a Main class that tests that the Cafe class works as expected.

6.a Above you will see a file called coffees.txt. Open it and check that is contains 5 names for types of coffee. Download it, or copy it to a new textfile and save it with the same name. Place coffees.txt in the same folder as the classes you will write for this task.

6.b Create a class called Main with a main method. 

6.c Create another class called Cafe. Give it an attribute called 'coffeeMenu' of type ArrayList\<String\>. 
(Later you will fill this ArrayList with the names of the coffees from the textfile).


6.c In the Cafe class, add a method <code>loadMenuData</code> 
Have the method load the coffees.txt file like this:
<code>File file = new File("coffees.txt) </code>  
(make sure that the path is right)


6.d In this step you will read from the file, using a Scanner object: Add the <code>file</code> instance to a new Scanner object. (This piece of code will need to be wrapped in a try -catch block)

The solution to this step is given below, but give it a go before peeping.
<details>
  <summary> The solution to this step:
  </summary>
  <code>try {

         Scanner scan = new Scanner(file); 

     }catch(FileNotFoundException e){

        System.out.println("File not found. Check path and filename");  

      }
</code>
</details>


6.e Inside the try block from the last step, you will now add this piece of code that loops over the lines of the textfile:


Use a while loop with hasNextLine() on the Scanner instance, to loop over the lines of the file and add the lines to the coffees ArrayList in this class.
<details>
  <summary> peep solution:
  </summary>
<code>

  while(scan.hasNextLine()){

        coffeeMenu.add(scan.nextLine());

  }

</code>      
</details>

6.g In the main method create a new instance of the Cafe class and call its <code>loadMenuData</code> -method.

6.h Still in the main method, print all the elements of the  attribute <code>coffeeMenu</code> of the Cafe instance you just created.
<details>
  <summary> Hint:</summary>
  you should use a for loop, and in the body of the loop use the <code>get()</code> method of ArrayList, to get hold of the item before printing it.  
</details>




