### Exercises with Scanner and Files
Today's tasks should be coded using the IntelliJ IDE. For each Task you will create a new project, as each task will require you to create a Main class with a main method. In some tasks you will write all the code in this main method, while in others you will be asked to make both a Main class with a main method in it (sometimes refered to as the "client class") and an "entity class" whithout a main method but with a constructor. The former is named so because it uses the services of the entity class.

---

## Task 1: Scanner basics
1.a: Start a new project and create a Main class with a main method.

1.b: In the main method start by printing a message to the user: "Please type your name".

1.c: Instantiate (create) a Scanner object for reading the command line (remember to import the Scanner class from the util library: <code>import java.util.Scanner; </code>)

1.d: Declare a String variable, <code>name</code> and assign the content of the scanner to it.

1.e: Print the value the user writes (print the <code>name</code> variable)

1.f: Print another message to the user: "Please type your age"

1.g: Declare another variable of type int, <code>age</code> and assign the content of the scanner to it (you may reuse the Scanner object created in 1.c).

1.h: Print the value the user writes (print the <code>age</code> variable)

1.i: Declare a third variable of type int. To this variable, assign the calculated number of years until the user can retire. You may assume retirement starts at 67 years. Print the result

---

## Task 2: Finish the GuessANumber class
2.a Open the java file above called GuessANumber.java and try to finish the code. Follow the steps written as comments in the <code>makeAGuess</code> method.

---

## Task 3. Textbased menu
3.a Create an entity class, Menu and a client class, Main with a main method.

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

3.e Create a method in the Menu class, <code>showMenu</code> that prints the sentence "Choose an option by typing the number associated". Then print each individual option on its own line.  
 <details>
  <summary>Hint</summary>
  <p>use a for-each loop for printing the options</p>
</details>

3.f. Still in the <code>showMenu</code> method, create a new Scanner object and then a variable <code>String choice</code> and assign it the user's input.

<details>
  <summary>Hint</summary>
  <p>
Scanner scan = new Scanner(System.in);
String choice = scan.nextLine();
</p>
</details>

3.g Let the <code>showMenu</code> method return the user's choice. 

<details>
  <summary>Hint</summary>
  <p>
  <code>return choice;</p></code>
  </p>
</details>


3.h In the main method call the showMenu method on the Menu instance, saving the return value (the user response) in a variable. Pass this variable as you call another method in the Main class, <code>doAction</code>, which you will write next.


3.i Create a method, <code>public static doAction(int choice)</code> in the Main class. The <code> int choice </code> parametre represents the user choice of option. 

3.j In the body of the method write a switch-case where:
   <li>case 1 will print "Starting the game now"</li>
   <li>case 2 will print "Fetching previously saved game data"</li>
   <li>case 3 will print "Game paused"</li>
   <li>case 4 will print "Ending game"</li>

---

## Task 4: load options
 
4.a Start a new textfile with the exact text given here:
"Expresso", "Americano" , "Macchiato", "Flat White",  "Latte"
Save it as a menu.csv file and placed it in the same folder as Cafe.java

4.b Create a class called Main with a main method. 

4.c Create another class called Cafe. Give it an attribute called 'coffees' of type ArrayList\<String\>. 
(Later you will fill this ArrayList with names of the coffees from the textfile).


4.c In the Cafe class, add a method <code>loadMenuData</code> 
Have the method load the file above called coffees.txt, like this 
<code>File file = new File("coffees.txt) </code>  
(make sure that the path is right)


4.d In this step you will read from the file, using a Scanner object: Add the <code>file</code> instance to a new Scanner object. (This piece of code will need to be wrapped in a try -catch block)

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


4.e Inside the try block from the last step, you will now add this piece of code that loops over the lines of the textfile:


Use a while loop with hasNextLine() on the Scanner instance, to loop over the lines of the file and add the lines to the coffees ArrayList in this class.
<details>
  <summary> peep solution:
  </summary>
<code>
  while(scan.hasNextLine()){
        coffees.add(scan.nextLine());
  }
</code>      
</details>

4.g In the main method create a new instance of the Cafe class and call its <code>loadMenuData</code> -method.

4.h Still in the main method, print all the elements of the  attribute coffees in the the Cafe instance you just created.
<details>
  <summary> Hint:</summary>
  you should use a for loop, and in the body of the loop use the <code>get()</code> method of ArrayList.   
</details>



## Task 5: write to file
[...]
