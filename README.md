# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
* Create a TicketMachine object on the object bench.
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
* Use `getBalance` to check that the machine has a record of the amount inserted.
	* You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.

### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket?
	* The value returned is 0.

### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior?
		* It will print out a receipt regardless of how much money you insert.
	* What happens if you insert too much money into the machine – do you receive any refund?
		* If you insert too much money into the machine, you can print out the receipt, but you won't get a refund.
	* What happens if you do not insert enough and then try to print a ticket?
		* If you do not insert enough money, you can still print out a ticket.

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	* Does the printed ticket look different?
		* The only difference is the price of the ticket.

### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.

	public class Student {};
	public class LabClass {};

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram?
		* The class did not function correctly and we see an error.
	* What error message do you get when you now press the compile button?
		* The error message says "<identifier> expected". 
	* Do you think this message clearly explains what is wrong?
		* The error is caused because the Class is trying to identify public which is a java reserved word.
	
### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.
	* It is possible to leave out the word public and it will still run.

### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
		* Fields: Price, Balance, Total
		* Constructors: TicketMachine
		* Metods: getPrice(), getBalance(), insertMoney(), printTicket()
	* Hint: There is only one constructor in the class.

### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
	*  The constructor has the same name as the class and has a return. Constructors usually don't have returns.

### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count;
private Student representative;
private Server host;
```

	* int
	* Student
	* Server


### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive;
private Person tutor;
private Game game;
```

	* boolean
	* Person
	* Game


### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
	  possible?
	  	* Ordering it differently is does not work because it uses a java reserved word and other combinations just doesn't work. The class diagram will show error.
	* Check by pressing the compile button to see if there is an error message.
	* Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration?
	* It is always necessary to have a semicolon at the end of a field declaration.
* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.
	* private int status;

### Exercise 2.16
* To what class does the following constructor belong?
```
public Student(String name)
```
	* This belongs in the Student class.

### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price)
```
	* The following constructor has two parameters. The title parameter has a String type, while the price parameter has a double type.

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?
	* Some of the types you might see in the 'Book' class will be String, int, or double.
* Can you assume anything about the names of its fields?
	* It might contain fields with names such as "title","author","page","year", and etc.
	
### Exercise 2.19 
* Suppose that the class Pet has a field called name that is of type String. Write an assignment statement in the body of the following constructor so that the name field will be initialized with the value of the constructor’s parameter.

	* name = petName;
	
### Exercise 2.21 
Compare the getBalance method with the getPrice method. What are the differences between them?
	* The only difference is the getBalance method returning the Balance, while the getPrice returns the price.
	
### Exercise 2.22 
If a call to getPrice can be characterized as ‘What do tickets cost?’, how would you characterize a call to getBalance?
	* How much money did you put in?

### Exercise 2.23 
If the name of getBalance is changed to getAmount, does the return statement in the body of the method need to be changed, too? Try it out within BlueJ.
	* You do not need to change it because it is just the name of the method. By naming convention, your method should 	     describe what action it will perform.
	
### Exercise 2.24 
Define an accessor method, getTotal, that returns the value of the total field.
	* The getTotal accessor method return information to the caller about the state of an object.

### Exercise 2.25 
Try removing the return statement from the body of getPrice. What error message do you see now when you try compiling the class?
	* "Missing return statement"

### Exercise 2.26 
Compare the method signatures of getPrice and printTicket in Code 2.1. Apart from their names, what is the main difference between them?
	The main difference is the type that is returned. getPrice will return an int, while the printTicket will return 	 nothing because it is void.
	
### Exercise 2.27 
Do the insertMoney and printTicket methods have return statements? Why do you think this might be? Do you notice anything about their headers that might suggest why they do not require return statements?
	* Both methods do not return any statements because they are void types, which means nothing will return,
	
### Exercise 2.28 
Create a ticket machine with a ticket price of your choosing. Before doing anything else, call the getBalance method on it. Now call the insertMoney method (Code 2.6) and give a non-zero positive amount of money as the actual parameter. Now call getBalance again. The two calls to getBalance should show different output because the call to insertMoney had the effect of changing the machine’s state via its balance field.

### Exercise 2.29 
How can we tell from just its header that setPrice is a method and not a constructor?
public void setPrice(int ticketCost)
	* Since it declares a return type you can tell it is a method. If there was not type then it would be a constructor.
### Exercise 2.30 
Complete the body of the setPrice method so that it assigns the
value of its parameter to the price field.

	public void setPrice(int ticketCost){
		price =ticketCost;}
		
### Exercise 2.31 
Complete the body of the following method, whose purpose is to
add the value of its parameter to a field named score.
  /**
   * Increase score by the given number of points.
   */
  public void increase(int points)
  {
  score = score + points;
 }
 
### Exercise 2.32 
Can you complete the following method, whose purpose is to sub- tract the value of its parameter from a field named price?
  /**
   * Reduce price by the given amount.
   */
  public void discount(int amount)
  {
	price = price - amount;
}

### Exercise 2.33 
Add a method called prompt to the TicketMachine class. This should have a void return type and take no parameters. The body of the method should print something like:
  Please insert the correct amount of money.
  
    public void prompt() {
    System.out.println("Please insert the right amount of money");
    }
    
### Exercise 2.34 
Add a showPrice method to the TicketMachine class. This should have a void return type and take no parameters. The body of the method should print something like:
The price of a ticket is xyz cents.
where xyz should be replaced by the value held in the price field when the method
is called.

    public void showPrice() {
    System.out.println("The price of a ticket is " + price + " cents.");
    }
    
### Exercise 2.35 
Create two ticket machines with differently priced tickets. Do calls to their showPrice methods show the same output, or different? How do you explain this effect?
	* The two machines show different prices because they are two different instances of the same class with their own      	  identity. Each has different prices because we set prices differently for both ticket machines.
	
### Exercise 2.36 
What do you think would be printed if you altered the fourth state- ment of printTicket so that price also has quotes around it, as follows?
  System.out.println("# " + "price" + " cents.");
  
  	* It will print out # price cents.
	
### Exercise 2.37 
What about the following version? System.out.println("# price cents.");

	* This will print out the same as the previous exercise, which is "# price cents."
	
### Exercise 2.38 
Could either of the previous two versions be used to show the price of tickets in different ticket machines? Explain your answer.

	* It will not be able to because the price is not a variable. The one we have are both hard coded statements that we 	       are printing.
	
### Exercise 2.39 
Modify the constructor of TicketMachine so that it no longer has a parameter. Instead, the price of tickets should be fixed at 1000 cents. What effect does this have when you construct ticket machine objects within BlueJ?

	* In BlueJ, we will not need to input the price for the ticket.
	
### Exercise 2.40 
Implement a method, empty, that simulates the effect of removing all money from the machine. This method should have a void return type, and its body should simply set the total field to zero. Does this method need to take any parameters? Test your method by creating a machine, inserting some money, printing some tickets, checking the total, and then emptying the machine. Is this method a mutator or an accessor?

	* This method is an accessor because we are accessing the variable total from outside the method and within the class.

### Exercise 2.41 
Implement a method, setPrice, that is able to set the price of tickets to a new value. The new price is passed in as a parameter value to the method. Test your method by creating a machine, showing the price of tickets, changing the price, and then showing the new price. Is this method a mutator?

	 * This method is an mutator because we are changing the value of total.
	 
### Exercise 2.42 
Give the class two constructors. One should take a single parame- ter that specifies the price, and the other should take no parameter and set the price to be a default value of your choosing. Test your implementation by creating machines via the two different constructors.

### Exercise 2.43 
Check that the behavior we have discussed here is accurate by creating a TicketMachine instance and calling insertMoney with various actual parameter values. Check the balance both before and after calling insertMoney. Does the balance ever change in the cases when an error message is printed? Try to predict what will happen if you enter the value zero as the parameter, and then see if you are right.

	* The balance does not change when you put a zero or negative number, which is what we want. It passes the validation 		test. If zero is the input, an error message will pop up.
	
### Exercise 2.44 
Predict what you think will happen if you change the test in insertMoney to use the greater-than or equal-to operator:
  if(amount >= 0)
Check your predictions by running some tests. What difference does it make to the behavior of the method?

	* By adding a greater-than or equal-to operator, the zero will be added to the balance and an error message will not 	       pop up.

### Exercise 2.45 
In the shapes project we looked at in Chapter 1 we used a boolean field to control a feature of the circle objects. What was that feature? Was it well suited to being controlled by a type with only two different values?

	* This was used for the visibility feature. It is well suited for this situation because there is only two options.
### Exercise 2.47
After a ticket has been printed, could the value in the balance field ever be set to a negative value by subtracting price from it? Justify your answer.

	* There is a check to prevent a negative value from happening with an if statement.
	
### Exercise 2.48 
So far we have introduced you to two arithmetic operators, + and –, that can be used in arithmetic expressions in Java. Take a look at Appendix D to find out what other operators are available.

	* There is also * , / , and %.

### Exercise 2.49 
Write an assignment statement that will store the result of multiply- ing two variables, price and discount, into a third variable, saving.

	* saving = price * discount;

### Exercise 2.50 
Write an assignment statement that will divide the value in total by the value in count and store the result in mean.

	* mean = total / count;

### Exercise 2.51 
Write an if statement that will compare the value in price against the value in budget. If price is greater than budget then print the message ‘Too expensive’, otherwise print the message ‘Just right’.

	* if(price >budget) {System.out.println("Too Expensive");}
		else {System.out.println("Just Right");}

### Exercise 2.52 
Modify your answer to the previous exercise so that the message if the price is too high includes the value of your budget.

	* if(price >budget) {System.out.println("Too Expensive because your budget is $ " + budget);}
		else {System.out.println("Just Right");}
		
### Exercise 2.53 
Why does the following version of refundBalance not give the same results as the original?
  public int refundBalance()
  {
balance = 0;
      return balance;
  }
What tests can you run to demonstrate that it does not?

	* In this version, you only return a balance of 0.

### Exercise 2.54 
What happens if you try to compile the TicketMachine class with
the following version of refundBalance?
  public int refundBalance()
  {
      return balance;
balance = 0; }
What do you know about return statements that helps to explain why this version does not compile?

	* You will get an "Unreachable Statement" error because anything after a return will not be read.
	
### Exercise 2.55 
Add a new method, emptyMachine, that is designed to simulate emptying the machine of money. It should both return the value in total and reset total to be zero.

	* public int emptyMachine() {
		int empty = total;
		total = 0;
		return empty; }
		
### Exercise 2.56 
Is emptyMachine an accessor, a mutator, or both?

	* emptyMachine is a mutator mutating the variables.
	
### Exercise 2.57 
Rewrite the printTicket method so that it declares a local variable, amountLeftToPay. This should then be initialized to contain the difference between price and balance. Rewrite the test in the conditional statement to check the value of amountLeftToPay. If its value is less than or equal to zero, a ticket should be printed, otherwise an error message should be printed stating the amount still required. Test your version to ensure that it behaves in exactly the same way as the original version.

	* public void printTicket()
	{
 	int amountLeftToPay = price - balance;
 	if(amountLeftToPay <= 0) {
 		// Simulate the printing of a ticket.
 		System.out.println("##################");
 		System.out.println("# The BlueJ Line");
 		System.out.println("# Ticket");
 		System.out.println("# " + price + " cents.");
 		System.out.println("##################");
 		System.out.println();
		
 		// Update the total collected with the price.
 		total = total + price;
 		// Reduce the balance by the prince.
 		balance = balance - price;
 		}
 	else {
 		System.out.println(
 		(amountLeftToPay) + " more cents is required.");
 		}

Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.
READ upto and INCLUDING section 2.15 of this chapter.
