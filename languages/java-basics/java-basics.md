# JAVA

MOOC Helsinki

## PART 1

### Variables

- `String` ”abcd”
- `int` : whole numbers
- `double` : numbers with decimals
- `boolean`

** Can only change int → double 

```java
// Must declare type before naming them
String text = "contains text";
int wholeNumber = 123;
double floatingPoint = 3.141592653;
boolean trueOrFalse = true;
```

### Printing & Input

- `System.out.println("Hello world!");` or `sout` + `tab`
- Ask for input :

```java
   		// Create a tool for reading user input and name it scanner
        Scanner scanner = new Scanner(System.in);

        // Print "Write a message: "
        System.out.println("Write a message: ");

        // Read the string written by the user, and assign it
        // to program memory "String message = (string that was given as input)"
        String message = scanner.nextLine() ;
```

- Read input of diff variable types

```java
//Integer
int value = Integer.valueOf(scanner.nextLine());

//Double
double value = Double.valueOf(valueAsString);

//Boolean
boolean value = Boolean.valueOf(scanner.nextLine());

```

### Calculation

Add & Multiply

```java
int first = 2;
int second = 4;

//add
System.out.println(first + second); //  6

//multiply
System.out.println(first * second); // 8
```

Division

> If the dividend or divisor (or both!) of the division is a double, the result is a double!
> 

```java

System.out.println(whenDividendIsFloat); // prints 1.5

double whenDivisorIsFloat = 3 / 2.0;
System.out.println(whenDivisorIsFloat); // prints 1.5

 //integer can be converted double  
```

> An integer can be converted into a double
> 

```java
int first = 3;
int second = 2;

double result1 = (double) first / second;
System.out.println(result1); // prints 1.5

double result = 1.0 * dividend / divisor;
System.out.println(result);

double result2 = first / (double) second;
System.out.println(result2); // prints 1.5\

// The last example produces an incorrectly rounded result, because the integer division is executed before the type casting.
double result3 = (double) (first / second);
System.out.println(result3); // prints 1.0
```

> Remainder `%`
> 

### Conditional Statements

- If, else if & else
    
    ```java
    int number = 3;
    
    if (number == 1) {
        System.out.println("The number is one");
    } else if (number == 2) {
        System.out.println("The given number is two");
    } else if (number == 3) {
        System.out.println("The number must be three!");
    } else {
        System.out.println("Something else!");
    }
    ```
    
- Comparison
    
    > The expression of a conditional statement may consist of multiple parts, in which the logical operators **and** `&&`, **or** `||`, and **not** `!` are used.
    > 

| <= | less than or equal to | > |  greater than
 |
| --- | --- | --- | --- |
| == | equal to | >=  | greater than or equal to |
| != | not equal to | <  | less than |

** cannot compare the equality of strings == , use `.equals`

```java
if (input.equals("a string")) {
    System.out.println("Great! ");
} 
```

## PART 2

### If Else

```python
//condition
if (value > 5) {
	    then? 
} else if (value < 0) { //
    // functionality when value is less than zero
    // and the value IS NOT larger than five
} else {  // otherwise
    // functionality otherwise
}
```

### While

To break the loop:

```python
while (true) {
    System.out.println("Input positive numbers.");
    int number = Integer.valueOf(scanner.nextLine());

    if (number == 0) {
        break;
    }

    if (number < 0) {
        System.out.println("Unfit number! Try again.");
        continue;
    }

    System.out.println("Your input was " + number);
```

Continue

> To skip the rest of the codes and return to the beginning of the loop
> 

### For

> For ( start, stop, step)
> 

for ( ***vartype var = start;***   ***loop condition;***   ***increased value***)

```java
for (int i = start; i < end; i++) {
    System.out.println(i);
```

```java
//print backward
for (int i = list.size() - 1; i >= 0; i--) {
            System.out.println(list.get(i));
```

### Method ( Function)

```java
// program code
        greet();
        
        // own methods
    public static void greet() {
        System.out.println("Greetings from the method world!");
```

- Introduce parameters
**Changing the value of the variables inside the method does not affect the value of the variable in the main method that has the same name.*

```java
//input parameter: numOfTimes
public static void sum(int first, int second) {
     int sum = first + second;
}     
```

- Return Values

> keyword `void` means that the method returns nothing.
Replace Keyword with type of return variable
> 

```java
public static int alwaysReturnsTen() {
    return 10;
}
```

- Can call a method within a method

## PART 3

### Lists (ArrayList)

> Resizable array that stores elements of the same type.
> 
- `import java.util.ArrayList` 
`ArrayList<Type> list = new ArrayList<>()`
- can be parameters for methods

**New, add, remove, get ,size, contain**

```java
ArrayList<Integer> integers = new ArrayList<>();
// adding
integers.add(10); 
integers.add(11); 

//retrieve (index 0)
integers.get(0); 

//size
integers.size();

//contains
list.contains("Second")

//remove(index OR literal value)
integers.remove(0); 
integers.remove(Integer.valueOf(10)) // if its string, can just type in: ..remove("banana")
```

**For each loop :** `for (Type name: List)`

- for everything in array list

```java
for( Integer num : integers) {
		}
```

### As a parameter for method

```java
public static void sprintSmallerThan(ArrayList<Integer> numbers, int threshold) {
```

### Arrays

> Fixed size container that stores elements of same type
> 
- can be parameters for methods

**New**
`type[ ] name - new int[num of elements]`

```java
int[] numbers = new int[3];
String[] strings = new String[5];
// OR
double[] arrayOfFloatingpoints = {1.20, 3.14, 10.0, 0.7};
```

**Add/access**
`numbers[0] = 2;`

### As a parameter of method

```java
public static void listElements(int[] integerArray) {
}
```

### String functions

- Split
    
    > Returns array
    > 
    > 
    > ```java
    > String text = "first second third fourth";
    > // returns string array: pieces
    > String[] pieces = text.split(" ");
    > ```
    > 
- Contains
`text.contains("can")`

## PART 4 - Classes

> Classes are blueprints for objects
> 

### Creating class

1. Name the class
2. Declare instances
3. Constructor 
- state var type of argument
1. Getters/Setters
- bc we cannot access private instances
2. Methods 
- Specifically, `toString` class will automatically be used when calling the class
These are the same: 
*System.out.println(antti.toString()); 
System.out.println(antti);*

```java
   		// 1. Instance variables 
public class Person {
			// 2. Instance variables 
    private String name;
    private int age;
    private int weight;
    
	    // 3. Constructor
	   public Person(String initialName) {
        this.age = 0;
        this.weight = 0;
        this.name = initialName;
      
      //4.
    public void setWeight(int newWeight) {
        this.weight = newWeight;
          
      //5.Methods
    public String toString() {
        return this.name + ", age " + this.age + " years";
    }
      
}
```

### Calling class

```java
// we create an object from the ArrayList class named integers
ArrayList<Integer> integers = new ArrayList<>();

// we create an object from the ArrayList class named integers
ArrayList<Integer> integers = new ArrayList<>();
```

### Using classes in lists

```java
for( String part: parts){
}
// must state vartrype (String)
// could also be a class (eg: Person) 

```

## PART 8 - HashMaps

> Use KEY to search for VALUE
> 

![image.png](JAVA%202ebab673c3c24e68b530e3876c3075fa/image.png)

### 

```java
import java.util.HashMap;
HashMap<String, String> numbers = new HashMap<>();

// ADD:put
numbers.put("00710", "Helsinki");

// RETRIEVE(value): get(key)
numbers.get(00710)

// Retrieve keys / values
numbers.keySet()
numbers.values()

//Check if contains key (boolean):
numbers.containsKey()
```

### TIPS

<aside>
💡

 1 key = 1 value

- If put ( alr existing key : new value) → Old value disappears
</aside>

<aside>
💡

If key is a string, recommended to “clean” it to search easily

- `string.toLowerCase().trim()`
</aside>

<aside>
💡

Hashmaps auto convert to reference variables
*risk : cannot convert null

![image.png](JAVA%202ebab673c3c24e68b530e3876c3075fa/image%201.png)

</aside>

### Other forms of Values (Array , Class etc)

### eg: ArrayList

---

```java
HashMap<String, ArrayList<Integer>> contacts = new HashMap<>();

// To add: first ensure there is a list
contacts.putIfAbsent("Police", new ArrayList<>());
this.contacts.get(Police).add(999)
```

### Hashcode/ Equals / Collision ??

This reliance on default methods such as `equals` is actually the reason why Java demands that variables added to ArrayList and HashMap are of reference type

## PART 9 - Class Inheritance / Interface

### Access Modifiers

| Private |  |
| --- | --- |
| Public |  |
| Protected | only visible to subclasses |
| Final |  |

### Inheritance

- `extends` keyword to define inheritance:
    
    <aside>
    📎
    
    The `Child` class automatically inherits all **non-private** variables and methods of the `Parent` class.
    
    </aside>
    
    - `super` can be used to refer to superclass methods / constructor (1st line)
    
    ```java
    class Parent {
        void display() {
            System.out.println("Parent display method");
        }
    }
    
    class Child extends Parent {
        @Override
        void display() {
            System.out.println("Child display method");
            super.display();  // Calls the display method in Parent class
        }
    }
    ```
    
    ### 
    

### Polymorphism

> The method to be executed is chosen based on the actual type of the object, which means the class whose constructor is called when the object is created.
> 
- If the method has no definition in that class, Java chooses the method from nearest superclass

```java
// Superclass
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}
```

Subclass

```java
// Subclass Dog
class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

// Subclass Cat
class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Cat meows");
    }
}
```

Main

```java

// Main class to demonstrate polymorphism
public class Main {
    public static void main(String[] args) {
		    Animal myAnimal;
        // Polymorphism in action
        myAnimal= new Dog();  // Animal reference, Dog object
        myAnimal.sound();   // Calls Dog's sound method
        
        
        myAnimal = new Cat();  // Animal reference, Cat object
        myAnimal.sound();   // Calls Cat's sound method
    }
}
```

### Interface

<aside>
💡

> Blueprint for classes
> 
- Classes must implement all methods in interface
- Interface defines: name , parameters, return values of method
</aside>

> Only contains method declarations, no body
> 
> 
> All instance variables are constants and are **`public`, `static`, and `final`**.
> 

Interface:

```java
public interface Animal {
    void sound(); // implicitly public and abstract
}
```

Implementing it:

```java
public class Dog implements Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}
```

- It can be a variable type/method parameters

```java
ArrayList<Animal> animals = new ArrayList<>();
animals.add(new Dog());
```

### Abstract classes

- Cannot be instantiated
- Can have both abstract (no body) and implemented method
- Blueprint for classes
- Use keyword `extends`
- Subclass is **REQUIRED** to implement the abstract method **UNLESS** it is a abstract class itself

```java
// Abstract class
abstract class Shape {
    // Concrete method
    void display() {
        System.out.println("This is a shape.");
    }

    // Abstract method
    abstract double area(); // No implementation, must be defined by subclasses
}

// Subclass: Circle
class Circle extends Shape {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    // Implementing the abstract method
    @Override
    double area() {
        return Math.PI * radius * radius; // Area of the circle
    }
}

// Subclass: Rectangle
class Rectangle extends Shape {
    private double length;
    private double width;

    public Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }

    // Implementing the abstract method
    @Override
    double area() {
        return length * width; // Area of the rectangle
    }
}

// Main class to demonstrate usage
public class Main {
    public static void main(String[] args) {
        Shape circle = new Circle(5.0);
        Shape rectangle = new Rectangle(4.0, 6.0);

        // Call the concrete method
        circle.display(); // Outputs: This is a shape.
        rectangle.display(); // Outputs: This is a shape.

        // Call the implemented abstract methods
        System.out.println("Circle area: " + circle.area()); // Outputs: Circle area: 78.53981633974483
        System.out.println("Rectangle area: " + rectangle.area()); // Outputs: Rectangle area: 24.0
    }
}

```

## PART 10 (i)  - Stream /Comparable

### Streams

### Basics of Streams

<aside>
💡

 Process data in a functional style, w operations like filtering and reducing, **without** modifying the underlying data structure (eg list)

</aside>

1. **Making Streams**
    - Formed from any obj that implements Collection interface( eg: ArrayList, HashMap)
2. **Operations**
    - Intermediate : return new stream , lazy, only evaluated when terminal operation called
    - Terminal : produced a result

```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6);
int result = numbers.stream()
                    .filter(n -> n % 2 == 0)
                    .map(n -> n * 2)
                    .reduce(0, Integer::sum);
System.out.println(result); // Output: 12 (2*2 + 4*2 + 6*2)
    
```

### Examples

![image.png](JAVA%202ebab673c3c24e68b530e3876c3075fa/image%202.png)

### Lambda expression

<aside>
💡

 a shorthand provided by Java

use arrow ( →)

</aside>

eg:

```java
// suppose we have a list of persons
// ArrayList<Person> persons = new ArrayList<>();

persons.stream()
    .map(person -> person.getFirstName())
    .distinct()
    .sorted()
    .forEach(name -> System.out.println(name));
```

 `reduce(*initialState*, (*previous*, *object*) -> *actions on the object*)`

```java
ArrayList<Integer> values = new ArrayList<>();
values.add(7);
values.add(3);
values.add(2);
values.add(1);

int sum = values.stream()
    .reduce(0, (previousSum, value) -> previousSum + value);
System.out.println(sum);
```

### Comparable Interface

<aside>
💡

 Ready made interface used to compare the current object with another object of the **same** type. NATURAL ORDERING

</aside>

1. **The class implementing `Comparable` must have a method `compareTo`**

```java
public class Member implements Comparable<Member> {
    private String name;
    private int height;
    
@Override
    public int compareTo(Member member) {
        if (this.height == member.getHeight()) {
            return 0;
        } else if (this.height > member.getHeight()) {
            return 1;
        } else {
            return -1;
        }
    }    
    // or: return this.height - member.getHeight();
    // or: return Integer.compare(this.height , other.height );
    //or: Collections.sort(persons, (p1, p2) -> Integer.compare(p1.getBirthYear(), p2.getBirthYear()));
```

1. **You can now call the .sort()** 
- Automatically calls `compareTo` ( just like how calling an object calls its `toString`)
- Directly modifies the list (unlike streams)

```java
 List<Member> members= new ArrayList<>();
 Collections.sort(members);
```

1. You can sort without implementing `Comparable`
- Pass a comparator inline directly:

```java
people.sort((p1, p2) -> Integer.compare(p1.getBirthYear(), p2.getBirthYear()));
```

### Multiple Comparison

<aside>
💡

When you need a different sorting order from `Comparable`or for custom sorting

</aside>

Implement `Comparator`  in separate class / in same class with lambdas.

```java
//Existing Code:
List<Person> people = new ArrayList<>();
people.add(new Person("Alice", 30, 1993));
people.add(new Person("Bob", 25, 1997));

```

```java
// NEW COMPARATOR:
public class PersonComparator implements Comparator<Person> {
    @Override
    public int compare(Person p1, Person p2) {
        int result = Integer.compare(p1.getBirthYear(), p2.getBirthYear());
        if (result == 0) {
            result = p1.getName().compareTo(p2.getName());
        }
        return result;
    }
} // you can jst call people.sort(new PersonComparator());

//Inline (Lambda)
people.sort(Comparator.comparingInt(Person::getBirthYear));

```

Multiple comparisons:

```java
  people.sort(Comparator.comparingInt(Person::getAge)
                .thenComparingInt(Person::getBirthYear));
```

![image.png](JAVA%202ebab673c3c24e68b530e3876c3075fa/image%203.png)

## PART 10 (ii) - Enum/Iterator

### Enumerate

<aside>
🔥

Special data typethat represents a group of constants (unchangeable variables)
eg: days of week/ card suites

</aside>

1. Defining a set of `enum`:

```java
public enum Suit {
    DIAMOND, SPADE, CLUB, HEART
```

1. Accessing 

```java
Day today = Day.MONDAY;
```

1. Used in classes

```java
public class Card {

    private int value;
    private Suit suit;

    public Card(int value, Suit suit) {
        this.value = value;
        this.suit = suit;
    }
    
    //to access
    if (first.getSuit() == Suit.SPADE) {
    System.out.println("is a spade");
```

- Comparison: use `==`
- Object References:

```java
public enum Color {
    RED("#FF0000"),     // RED constant has color code "#FF0000"
    GREEN("#00FF00"),
    BLUE("#0000FF");
    //constants (constructor parameters)
private String code;        //object reference variable 
                            //'code' is a field that holds the parameters
                            
                            
// Constructor that assigns the color code                          
private Color(String code) { 
        this.code = code;
}

// Getter method to retrieve the color code
public String getCode() {
        return this.code;  
    }

```

 

### Iterator

<aside>
🔥

 **`Iterator`** is a key part of the Collections Framework, allowing traversal through elements of a collection (e.g., **`ArrayList`**, **`HashSet`**) one at a time!

</aside>

### Important methods:

```java
public void print(){
    Iterator<Card> iterator = cards.iterator(); // make iterator

    while (iterator.hasNext()) {              // boolean, true is have more
        Card nextInLine = iterator.next();    // get the next value
        System.out.println(nextInLine);
    }
}
```

| Method | Explain |
| --- | --- |
| `.remove` | removes from list directly |
|  |  |

FYI:

- Allows for safe removal during iteration
- Cannot use foreach to remove as this alr thinks there is a preset size.

## PART 11 - Exceptions

<aside>
🔥

Events that disrupt the normal flow of a program during runtime.

</aside>

**Types of exceptions:**

| Checked  | Unchecked | Errors |
| --- | --- | --- |
| Must be declared or handled | don’t need explicit handling | serious problems |
| has red squiggly line |  | Examples: `OutOfMemoryError`, `StackOverflowError` |

![image.png](JAVA%202ebab673c3c24e68b530e3876c3075fa/image%204.png)

**Handling exceptions:**

```java
try {
    // Risky code
} catch (Exception e) {
    // Handle exception
} finally {
    // Cleanup code
}
```

**Throwing Exceptions:**

```java
if (value < 0) {
    throw new IllegalArgumentException("Value must be positive");
}
```

### Eg

1. a single `try` block with multiple `catch` blocks to handle different types of exceptions
- The order of catch matters!

```java

    public static void main(String[] args) {
        try {
            int[] numbers = {1, 2, 3};
            System.out.println(numbers[5]); // May throw ArrayIndexOutOfBoundsException
            int result = 10 / 0;           // May throw ArithmeticException
            
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Index is out of bounds!");
        } catch (ArithmeticException e) {
            System.out.println("Cannot divide by zero!");
        } catch (Exception e) {
            System.out.println("An unexpected error occurred: " + e.getMessage());
        }
    }
```

1. Diff methods having similar exceptions:

```java
public class PropagateExample {
    public static void methodA() throws ArithmeticException {
        int result = 10 / 0; // ArithmeticException
    }

    public static void methodB() throws ArrayIndexOutOfBoundsException {
        int[] numbers = {1, 2, 3};
        System.out.println(numbers[5]); // ArrayIndexOutOfBoundsException
    }

    public static void main(String[] args) {
        try {
            methodA();
            methodB();
            
        } catch (ArithmeticException e) {
            System.out.println("Error: Cannot divide by zero!");
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Error: Index out of bounds!");
        }
    }
}
```