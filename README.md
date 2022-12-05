# PolymorphismAndInheritance
PolymorphismAndInheritance Practice Assignment for TEKJava Cohort


303.6.1- Practice Assignment
Polymorphism and Inheritance
Canvas Submission Guideline:
● Points:100
● Assignment Type: Non-graded (This assignment does not count toward the
final grade.), Complete/Incomplete
● Submission Type:
○ Document File or Source Code Files
● Instructions: Please include the following deliverables in your submission -
○ Please submit your source code using the Start Assignment button in
the top right corner of the assignment page in Canvas.
1
Monster and its Subclasses
Scenario: In our game app, we have many types of monsters that can attack. You
will design a superclass called Monster and define the method of attack() in the
superclass. You will design subclasses called FireMonster, WaterMonster, and
StoneMonster. The subclasses will then provide their actual implementation. In
the main program, we declare instances of the superclass, substitute them with
the actual subclass, and invoke the method defined in the superclass.
Hint: The main() method is following:
public class TestMonster {
public static void main(String[] args) {
// Program at the "interface" defined in the superclass.
// Declare instances of the superclass, substituted by subclasses.
Monster m1 = new FireMonster("r2u2"); // upcast
Monster m2 = new WaterMonster("u2r2"); // upcast
Monster m3 = new StoneMonster("r2r2"); // upcast
// Invoke the actual implementation
System.out.println(m1.attack()); // Run FireMonster's attack()
System.out.println(m2.attack()); // Run WaterMonster's attack()
System.out.println(m3.attack()); // Run StoneMonster's attack()
// m1 dies, generate a new instance and re-assign to m1.
m1 = new StoneMonster("a2b2"); // upcast
System.out.println(m1.attack()); // Run StoneMonster's attack()
// We have a problem here!!!
Monster m4 = new Monster("u2u2");
System.out.println(m4.attack()); // garbage!!!
2
}
}
Output:
Attack with fire!
Attack with water!
Attack with stones!
Attack with stones!
!^_&^$@+%$* I don't know how to attack!
3

303.6.3- Practice Assignment - Polymorphism and
Interface
Canvas Submission Guideline:
● Points:100
● Assignment Type: Non-graded (This assignment does not
count toward the final grade.), Complete/Incomplete
● Submission Type:
○ Document File or Source Code Files
● Instructions: Please include the following deliverables in
your submission -
○ Submit your source code using the Start
Assignment button in the top right corner of the
assignment page in Canvas.
1
Objective
After completing the hands-on lab, you will be able to:
● Implement interfaces in your program.
● Apply polymorphism concept using the interface.
Requirements
Scenario: A library needs to develop an online application for two types of users/roles, Adults
and children. Both of these users should be able to register an account. Any user under 12 years
of age will be registered as a child, and they can borrow a “Kids” category book for 10 days,
whereas an adult can borrow “Fiction” category books, which need to be returned within 7
days.
Note: In the future, more users/roles might be added to the library where similar rules will be
enforced.
Develop interfaces and classes for the categories mentioned above.
Problem Statement 1:
1. Create an interface LibraryUser with the following methods declared,
Method Name
registerAccount
requestBook
2. Create 2 classes “KidUsers” and “AdultUser” which implement the LibraryUser interface.
3. Both the classes should have two instance variables as specified below.
Instance variables Data type
age int
bookType String
4. The methods in the KidUser class should perform the following logic.
2
1. registerAccount : if age <= 11, a message displaying “You have successfully
registered under a Kids Account” should be displayed in the console.
If(age > 11), a message displaying, “Sorry, Age must be less than 12 to register
as a kid” should be displayed in the console.
2. requestBook : if bookType is “Kids”, a message displaying “Book Issued successfully,
please return the book within 10 days” should be displayed in the console.
else, a message displaying, “Oops, you are allowed to take only kids books”
should be displayed in the console.
5. The methods in the AdultUser class should perform the following logic.
1. registerAccount : if age >= 12, a message displaying “You have
successfully registered under an Adult Account” should be displayed in the
console.
If age <= 11, a message displaying, “Sorry, Age must be greater than 12 to
register as an adult” should be displayed in the console.
2. requestBook : if bookType is “Fiction”, a message displaying “Book Issued
successfully, please return the book within 7 days” should be displayed in the
console.
else, a message displaying, “Oops, you are allowed to take only adult
Fiction books” should be displayed in the console.
6. Create a class “LibraryInterfaceDemo.java” with a main() method that performs the below
functions,
Test case #1:
● Create an instance of KidUser class.
● Set the age as specified in the below table and invoke the registerAccount()
method of the KidUser object
Age
10
18
3
● Set the book Type as specified in the below table and invoke the
requestBook() method of the KidUser object,
BookType
“Kids”
“Fiction”
Test case #2:
● Create an instance of the AdultUser class.
● Set the age as specified in the below table and invoke the registerAccount()
method of the AdultUser object
Age
5
23
● Set the book Type as specified in the below table and invoke the
requestBook() method of the AdultUser object
BookType
“Kids”
“Fiction”
4
