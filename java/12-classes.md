# Classes

Let's start out with some guiding questions.

- What is a car?
- What properties do all cars have?
- What can all cars do?

Car
| Properties     | Actions |
|----------------|---------|
| color          | drive   |
| speed          | turn    |
| num wheels     | brake   |
| num passengers | honk    |
| ...            | ...     |

## Make it Classy

A __class__ defines the properties (what something is) and the methods (what something does) of an __Object__. In other words, an __Object__ is a thing with two characteristics, properties and behavior, and classes are templates used to create these objects.

In the above example, the Car object had properties such as color, speed, etc., and behaviors of drive, turn, etc. Let's write a class to create __instances__, unique copies of a class, of Cars.

```java
public class Car {
    int size;

    // ...
}
```

We can use this class as a blueprint to create different instances of Cars. This example shows how you can define properties, or __attributes__ of classes; `size` is an attribute of a Car.

```java
public class Car {
    int size;
    int speed;

    public Car (int a, int b) {
        size = a;
        speed = b;
        openDoor();
    }

    public void openDoor() {
        // code...
    }
}
```

What are the attributes of this class? What are the actions (aka methods)?

In the above example, there is also a __constructor__.

The role of a constructor is to specify the attributes of an instance of an object when it is first created.

The constructor always has the same name as the class, in this case `Car`.

## Creating Instances of Objects

By themselves, classes do not do anything. Remember, they are only the blueprints that define objects. In order to use classes, we need to create instances of that class.

We can do so using the `new` keyword.

Continuing with the above class example,
```java
Car toyota = new Car(5, 3);
```

This creates a Car, named `toyota`, that has a `size` of 5 and a `speed` of 3. The `size` and `speed` are set because the constructor for Car is run when a Car is created; `size` is set to the first input, `5`, and `speed` is set to the second input, `b`.

The syntax for creating an instance for any class is
```java
Class name = new Class(<inputs if there are>);
```

## What Are You?

To get an attribute from an object or to make an instance of an object do something, we use the dot notation.

To get the speed of the Car instance we just created, we would do something like:
```java
int x = toyota.speed;
```

To drive it:
```java
toyota.drive();
```

In general, dot notation looks like:
```java
<object name>.<variable or method name>;
```

## Remember?

Remember Scanner? Unknown to you, we were creating Scanner objects and using them in our code.

```java
Scanner sc = new Scanner(System.in);
```

## Writing a Class

Remember the "hello world" programs we wrote in the beginning of this course? You were actually creating a class that did nothing but print "Hello world!". The same rules for those programs apply to our classes: your filename must match the class name, your main method runs the code, and everything else is used by the main method to run the code.

```java
public class Car {

    public int speed;  // visibility modifiers can be attached to attributes!
    private int size;

    public Car(int a, int b) { // constructors should always be public--why?
        speed = a;
        size = b;
    }

    // method of the Car class
    public void drive() {
        speed++;
    }

    // this is the code that runs
    public static void main( String[] args ) {
        Car toyota = new Car(3, 5);
        toyota.drive();
        System.out.println(toyota.speed);
    }

}
```

What is the output of this program?

Note that not all classes have to have a main method. Only classes that you intend to run should have a main method. This may not make much sense now, but we'll return to this idea in our next project.

## Why Classes

Let's say you're writing a application that has a similar GUI with different content on every page. Wouldn't it be a waste of time and resources to write the code to draw the GUI for every single page? Instead, if you had a Page class with attributes for where buttons/text should go, and methods that keep track of user clicks, you could save yourself a lot of time.

Especially for large projects, creating classes can save you a lot of time. We will examine this in our next project.

## Practice

Write a class `Computer` that contains the following attributes: `size`, `weight`, `model`, and `isFast` with the appropriate data types. It should also contain the following methods: `upgrade(x)`, which should decrease the size and weight by `x`; `downgrade(x)`, which should increase the size and weight by `x`; and `toggleQuantumState()`, which should change `isFast` to the opposite of `isFast`. All of the attributes should be set when an instance is created (cough sounds like a job for a constructor cough).

Then, in a main method, create an instance of your computer called `machine`. Give it a `size` of `2`, `weight` of `3.5`, `model` of `"dell"`, and `isFast` to `false`.

Call the machine's `upgrade` method with an input of 5, and call `toggleQuantumState()`. Print out all of the `machine`'s attributes. Are they as you expected? Sample code is the assets directory of this course.

## More on Constructors

### Default


### Overloaded

## Multi-file Programs

## String

## Practice