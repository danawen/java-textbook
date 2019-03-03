# Interfaces

## Reading Material

We will cover all of the topics below during class. For review and further reading, check out these sections from the Java Tutorials handbook.

- [Intro to Interfaces](https://docs.oracle.com/javase/tutorial/java/IandI/createinterface.html)
- [Defining an Interface](https://docs.oracle.com/javase/tutorial/java/IandI/interfaceDef.html)
- [Implementing an Interface](https://docs.oracle.com/javase/tutorial/java/IandI/usinginterface.html)
- [Using an Interface as a Type](https://docs.oracle.com/javase/tutorial/java/IandI/interfaceAsType.html)
- [Default Methods](https://docs.oracle.com/javase/tutorial/java/IandI/defaultmethods.html)
- [Abstract Classes vs. Interfaces](https://docs.oracle.com/javase/tutorial/java/IandI/abstract.html)

## Interfaces

In the Java programming language, an interface is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. Method bodies exist only for default methods and static methods. Interfaces cannot be instantiated—they can only be implemented by classes or extended by other interfaces.

```java
public interface Pet {
  
  String getName();

  String speak();

  default String sleep(){
    return "zzz!";
  }

}

public class Cat implements Pet {
  String name;
  int livesLeft;

  public Cat(String name){
    this.name = name;
    this.livesLeft = 9;
  }

  public String getName(){
    return name;
  }

  public int getLivesLeft(){
    return livesLeft;
  }

  public String speak(){
    return "Meow";
  }

  public String sleep(){
    return "prrr, prrr";
  }
}



public class Dog implements Pet {
  String name;
  String breed;

  public Dog(String name, String breed){
    this.name = name;
    this.breed = breed;
  }

  public String getName(){
    return name;
  }

  public String speak(){
    return "Woof";
  }
}

```


<iframe height="400px" width="100%" src="https://repl.it/@kevincolten1/FarawayEvilProgrammers?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
