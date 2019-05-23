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
	Nothings changes
	* What happens if you insert too much money into the machine – do you receive any refund?
	Still nothing
	* What happens if you do not insert enough and then try to print a ticket?
	Still also nothing

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	* Does the printed ticket look different?
	no it does not

### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
public class Student {

	inner part

}

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?
Yes it does matter, it will not compile otherwise

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram?
		it becomes cross hatched with red 
	* What error message do you get when you now press the compile button?
		<identifier> expected
	* Do you think this message clearly explains what is wrong?
		yes, because public is the identifier for the type of class

### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.
It is possible

### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
	* Hint: There is only one constructor in the class.
Fields: price balance totals
Constructor: ticketCost
Methods: getPrice(), getBalance(), insertMoney(), printTicket()

### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
It will only return values or tickets 

### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count;
This is an integer

private Student representative;
This is a string

private Server host;
This is a string
```

### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive;
This is named alive 

private Person tutor;
This is named tutor

private Game game;
This is named game
```
### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
Yes it matters

* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible?
Yes it turns red and gets cross hatched
	* Check by pressing the compile button to see if there is an error message.
	* Make sure that you reinstantiate the original version after your experiments!
You can leave off the class designation but int and getPrice need to be in the original order.  Changing them will throw errors in the editor and diagram

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration?
* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.
Yes, it signifies that the declaration is over. 

### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.
private int status

### Exercise 2.16
* To what class does the following constructor belong?
```
public Student(String name)
```
student

### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price)
```
Two and the types are string and double

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?
* Can you assume anything about the names of its fields?
The book field types could include strings for author, title and publish date.  It could have  a double for the price of a book.  It could have a double for dewey number or isbn number.  

Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.
READ upto and INCLUDING section 2.15 of this chapter.

2.19
Public Pet(String petsName)
{
	name = petsName;
}

2.21
getBalance() is dynamic and the return change depending amount of money paid so fae.  getPrice() is static and once initiated will remain the same

2.22
It can be characterized as "How much have I paid already?"

2.23
No it doesn't have to be changed

2.24
Public int getTotal() 
{	
	return total;
}

2.25
You get "missing return statement" error in both cases

2.26
The main difference is that getPrice() returns the price of a ticket and printTicket() prints out a ticket.

2.27
No, because they have the word void in the header

2.29
Because of the void in the header

2.30
public void setPrice(int ticketCost)
{
	price = ticketCost + price;
}

2.31
public void increase(int points)
{
	score = score + points;
}

2.32
Public void discount (int amount)
{
	price = price - amount;
}

2.33
See blueJ

2.34
See bluej

2.35
They show different outputs because the showPrice() references the price variable

2.36
It would print out the string price 

2.37
It would print out # price cents as a string

2.38
No because its still a string 

2.39
It fixes the price of a ticket at 1000

2.40
It is a mutator 

2.41

2.43
It will print out 'use a positive amount'

2.44
It will execute the if statement, as it will become inclusive of 0 

2.46
In the naive ticket machine, the end of the printTicket() method, the total was added with the balance, which was then cleared, regardless of remaining money inside it. Now, however, the method adds price to the total, and reduces price from the balance, thereby eliminating the need to clear the balance field.

2.47
No, because insertMoney() specifies that amount>=0

2.48
* = multiplication
/ = division
% = modulus

2.49 
public Store()
{
int saving;
saving = price*discount;
}

2.50
public Mean(int mean)
{
mean = total/count;
}
	
2.51
public void shouldBuy()
{
if(price>budget)
System.out.printIn(“Too Expensive”);
else return
System.out.printIn(“Just Right”);
}

2.52
public void shouldBuy()
{
if(price>budget)
System.out.printIn(“Too Expensive, Current Budget:” + budget);
else return
System.out.printIn(“Just Right”);
}

2.53
Because it clears the balance]

2.54
It won’t compile because methods that return values always have to have the return block at the end of the method.

2.56
Its a mutator





