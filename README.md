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

0

### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior?

The balance doesn't seem to matter

	* What happens if you insert too much money into the machine – do you receive any refund?

No

	* What happens if you do not insert enough and then try to print a ticket?

You get a ticket anyway

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	* Does the printed ticket look different?

	Yes. It has a different price listed

### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.

Public Student(string name, int age)
{

}

Public LabClass(args)
{

}

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?


* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram?
	
	Yes

	* What error message do you get when you now press the compile button?

	"invalid method declaration; return type required"

	* Do you think this message clearly explains what is wrong?

	not particularly

### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.

It is. It doesn't like adding 'private', though.

### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
	* Hint: There is only one constructor in the class.

FIELDS
	int price
	int balance
	int total
CONSTRUCTORS
	TicketMachine(int)
METHODS
	int getPrice()
	int getBalance()
	void insertMoney(int)
	void printTicket()
	

### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?

It doesn't have a type

### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count;  >> int
private Student representative;  >> Student
private Server host;  >> Server
```


### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive;  >> alive
private Person tutor;  >> tutor
private Game game;  >> game
```
### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible?
	* Check by pressing the compile button to see if there is an error message.
	* Make sure that you reinstantiate the original version after your experiments!

It matters. It won't compile otherwise.

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration?
* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.

 Yes. Yes it is.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.

	private int status;

### Exercise 2.16
* To what class does the following constructor belong?
```
public Student(String name)
```
 Student


### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price)
```
	Two constructors. One is a String, the other is a double.

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?
* Can you assume anything about the names of its fields?

The Book class will probably have a field of type String and a field of type double.

Short answer, no. Longer answer, the string field is probably named something similar to, but not exactly "title", and the double field is probably named something similar to, but not exactly "price".

Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.
READ upto and INCLUDING section 2.15 of this chapter.


Exercise 2.19
	name = petsName;


Exercise 2.20
	challenge exercise

	because price is declared inside the constructor, it creates a new variable within the scope of the constructor. ticketCost will be assigned to the new "constructor-price" rather than the "field-price" and so will not persist after the constructor ends. The actual price of the ticket will remain 0.


Exercise 2.21
	they return the value of different fields

Exercise 2.22
	"what is the current balance, in cents?"

Exercise 2.23
	no

Exercise 2.24
	public int getTotal()
	{
		return total;
	}

Exercise 2.25
	"missing return statement"

Exercise 2.26
	getPrice returns int, printTicket "returns" void

Exercise 2.27
	they don't have return statements. I would speculate that this is because they have return type void

Exercise 2.28
	they do indeed show different output

Exercise 2.29
	the setPrice has a type (void)

Exercise 2.30
	public void setPrice(int ticketCost){
		price = ticketCost;
	}

Exercise 2.31
	public void increase(int points){
		score += points;
	}

Exercise 2.32
	public void discount(int amount){
		if(amount < price){
			price -= amount;
		}
		else {
			price = 0;
		}
	}

Exercise 2.33
    public void prompt(){
        System.out.println("Please insert the correct amount of money");
    }

Exercise 2.34
    public void showPrice(){
        System.out.printf("The price of a ticket is %d cents.\n",price);
    }

Exercise 2.35
	They show different output because the two objects have different values for their respective price variables.

Exercise 2.36
	It would print the word "price" rather than the value of the object-variable price

Exercise 2.37
	the same as question 2.36

Exercise 2.38
	yes. The way the machines are set up, there is effectively no price.
	neither of the two versions are suitable for printing the value of the object-variable price, however.

Exercise 2.39
	BlueJ no longer asks for a value for ticketCost when it constructs a TicketMachine

Exercise 2.40
	The method does not need any parameters (although it probably should have one as a security code to ensure that not just anyone can take all the money)
	The method is a mutator

Exercise 2.41
	The method is a mutator

Exercise 2.42
	Implemented

Exercise 2.43
	If a negative amount is entered, the console prints a message, and balance does not change
	Prediction: if zero is entered, the console will print a message
	Result: vindication

Exercise 2.44
	Prediction: the method will act the same, except that a message will not print if 0 is entered. Instead, 0 will be added to the balance (so it still won't change, because zero)
	Result: vindication

Exercise 2.45
	a boolean was used to control whether the circle was visible or not
	the visibilty toggle was well suited to being controlled by a type with only two different values

Exercise 2.46
	in version 1.0, total is increased by balance and balance is reset to 0. In version 2.0, total is increased by price and balance is reduced by price.
	it appears to be thus

Exercise 2.47
	No. When printTicket() is called, balance is reduced by price IF balance is at least equal to price. Otherwise an error message is printed and balance is left unchanged. Balance cannot be reduced by more than its value, and so cannot be set to negative using the printTicket() method.

Exercise 2.48
	Appendix D not in pdf

Exercise 2.49
    public int getSavings(int discount){
        
        double savingD = price * ((double)discount/100);
        int saving = (int)Math.floor(savingD);
        return saving;
    }

Exercise 2.50
    public double divide(int count){
        double mean = (double)total / (double)count;
        return mean;
    }

Exercise 2.51
    public void checkBudget(int budget){
        if(price > budget){
            System.out.println("Too expensive");
        }
        else {
            System.out.println("Just right");
        }
                
    }

Exercise 2.52
    public void checkBudget(int budget){
        if(price > budget){
            System.out.println("Too expensive");
            System.out.printf("Budget is only %d cents\n",budget);
        }
        else {
            System.out.println("Just right");
        }
                
    }

Exercise 2.53
	because balance has been set to zero before it is returned, so this method will always return 0
	To demonstrate, call the alternate refundBalance() when balance is not 0
	
Exercise 2.54
	two error messages: "unreachable statement" and "missing return statement"
	method ends and exits when return statement is reached, so the compiler is helpfully reminding you that code after the return statement makes no sense

Exercise 2.55
    public int emptyMachine(){
        int curTotal = total;
        total = 0;
        return curTotal;
    }

Exercise 2.56
	emptyMachine is a mutator. You can't use it to get the value of total because when it is used, the value of total becomes different from what is returned (unless total was already 0)

Exercise 2.57
    public void printTicket2(){
        int amountLeftToPay = price - balance;
        if(amountLeftToPay > 0){
            System.out.printf("You must insert at least %d cents\n",price-balance);
        }
        else {
            total = total + price;
            balance = balance - price;
        }
    }

Exercise 2.58
	challenge exercise

	the only method needed would be a set price method