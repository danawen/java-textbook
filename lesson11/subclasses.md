# Subclasses and Inheritance

## Reading Material

We will cover all of the topics below during class. For review and further reading, check out these sections from the Java Tutorials handbook.

- [Intro to Subclasses & Inheritance](https://docs.oracle.com/javase/tutorial/java/IandI/subclasses.html)
- [Overriding Methods](https://docs.oracle.com/javase/tutorial/java/IandI/override.html)
- [Polymorphism](https://docs.oracle.com/javase/tutorial/java/IandI/polymorphism.html)
- [The "super" Keyword: Accessing Superclass Methods & Constructors](https://docs.oracle.com/javase/tutorial/java/IandI/super.html)
- [Abstract Methods & Classes](https://docs.oracle.com/javase/tutorial/java/IandI/abstract.html)
- [Final Classes & Methods](https://docs.oracle.com/javase/tutorial/java/IandI/final.html)

## Example: Superclass & Subclass

The example below illustrates subclasses and inheritance. The superclass (parent class) `Bicycle` contains fields and methods that are inherited by the subclass (child class) `MountainBike`.

```java
public class Bicycle {
        
    // the Bicycle class has three fields
    public int cadence;
    public int gear;
    public int speed;
        
    // the Bicycle class has one constructor
    public Bicycle(int startCadence, int startSpeed, int startGear) {
        gear = startGear;
        cadence = startCadence;
        speed = startSpeed;
    }
        
    // the Bicycle class has five methods
    
    public void setCadence(int newValue) {
        cadence = newValue;
    }
        
    public void setGear(int newValue) {
        gear = newValue;
    }
        
    public void applyBrake(int decrement) {
        speed -= decrement;
    }
        
    public void speedUp(int increment) {
        speed += increment;
    }
    
    public void printDescription(){
        System.out.println("\nBike is in gear " + this.gear
        + " with a cadence of " + this.cadence +
        " and travelling at a speed of " + this.speed + ". ");
    }
        
}
```
A class declaration for a `MountainBike` class that is a subclass of `Bicycle` might look like the code below.
`MountainBike` inherits all the fields and methods of `Bicycle` and adds the field `seatHeight` and methods to get and set it (mountain bikes have seats that can be moved up and down as the terrain demands).
The `printDescription()` method demonstrates the concept of _polymorphism_: Subclasses of a class can define their own unique behaviors and yet share some of the same functionality of the parent class.


```java
public class MountainBike extends Bicycle {
        
    // the MountainBike subclass has one field
    public int seatHeight;

    // the MountainBike subclass has one constructor
    public MountainBike(int startHeight, int startCadence,
                        int startSpeed, int startGear) {
        super(startCadence, startSpeed, startGear); // call the superclass constructor
        seatHeight = startHeight;
    }   
        
    // the MountainBike subclass has two methods
    
    public String getSeatHeight(){
      return this.seatHeight;
    }
    
    public void setSeatHeight(int newValue) {
        seatHeight = newValue;
    }
    
    public void printDescription() {
        super.printDescription(); // call superclass method
        System.out.println("The MountainBike has a seat height of " +
            getSeatHeight() + ".");
    }

}
```
