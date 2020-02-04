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
Answer: 0

### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior?
			Answer: getTotal() increments current balance without adding cash, the machine doesn't give change.  It outputs to the user the message of how much the machine has gathered (An incorrect amount at that, because it eats your change) instead of the user's remaining balance.

	* What happens if you insert too much money into the machine – do you receive any refund?
			Answer: It eats your balance when it calls printTicket().

	* What happens if you do not insert enough and then try to print a ticket?
		You still get your ticket, but the money entered is spent.

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	* Does the printed ticket look different?
		Answer: The output message's price is different.

### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
	Answer:
		public class Student
		public class LabClass

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?
	Answer: Yes, `class public TicketMachine` does not compile.

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram?
			Answer: Yes, it is criss-crossed.

	* What error message do you get when you now press the compile button?
			Answer: `<identifier> expected`, `illegal start of expression` and `invalid method declaration; return type required`

	* Do you think this message clearly explains what is wrong?
			Answer: Somewhat, I don't really know what an `<identifier>` is but I can Google it

### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.

### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
	* Hint: There is only one constructor in the class.
		Answer:
			`field`: price, balance, total, ticketNumber
			`constructor`: public TicketMachine(Integer ticketCost)
			`methods`: getPrice, getTicketNumber, getBalance, insertMoney, calculateTotal, incrementTicketNumber, printTicket

### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
	Answer: The constructor initializes the fields such as balance or ticketNumber.

### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count;
	Answer: int
private Student representative;
	Answer: Object
private Server host;
	Answer: Object
```

### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive;
	Answer: alive
private Person tutor;
	Answer: tutor
private Game game;
	Answer: game
```
### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
	Answer: Yes.  Changing the order will cause a syntax error.

* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible?
	* Check by pressing the compile button to see if there is an error message.
	* Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration?
* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.

### Exercise 2.16
* To what class does the following constructor belong?
```
public Student(String name)
```

### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price)
```

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?
* Can you assume anything about the names of its fields?

READ upto and INCLUDING section 2.15 of this chapter.
