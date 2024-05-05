# Dart Object Oriented Programming

[for read(source):](https://dart-tutorial.com/object-oriented-programming/#google_vignette)

1. OOP In Dart


Object Oriented Programming (OOP) is a programming paradigm that uses objects and their interactions to design and program applications.
OOP is based on objects, which are data structures containing data and methods.
OOP is a way of thinking about programming that differs from traditional procedural programming.
OOP can make code more modular, flexible, and extensible.
OOP can help you to understand better and solve problems.


Features Of OOP

*     Class
*     Object
*     Encapsulation
*     Inheritance
*     Polymorphism
*     Abstraction


Advantages

*     It is easy to understand and use.
*     It increases reusability and decreases complexity.
*     The productivity of programmers increases.
*     It makes the code easier to maintain, modify and debug.
*     It promotes teamwork and collaboration.
*     It reduces the repetition of code.

## Class In Dart

In object-oriented programming, a class is a blueprint for creating objects. A class defines the properties(field,attrributs) and methods(functions) that an object will have.



*     The class is declared using the class keyword.
*     The class is a blueprint for creating objects.
*     The class body consists of properties and methods.
*     The properties are also known as fields, attributes, or data members.
*     The methods are also known as behaviors, or member functions.

example:

	class Book {
	  String? name;
	  int? author;
	  int? prize;
	
	  void display() {
	    print("Book name: $name.");
	    print("Book author: $author.");
	    print("Book prize: $prize.");
	  }
	}

## Object In Dart

Object is a self-contained unit of code and data. Objects are created from templates called classes. An object is made up of properties(variables) and methods(functions). An object is an instance of a class.
Instantiation is the process of creating an instance of a class.

**Syntax**

ClassName objectName = ClassName();

Example:

	class Camera {
	      String? name;
	      String? color;
	      int? megapixel;
	    
	    
	      void display() {
	        print("Name: $name");
	        print("Color: $size");
	        print("Megapixel: $megapixel");
	      }
	    }
	
	    void main(){
	        // Here camera is object of class Camera. 
	        Camera camera1 = Camera();
	        camera1.name = "GoPro";
	        camera1.megapixel = 1080;
	        camera1.display();
	        Camera camera2 =new Camera();
	        camera2.name = "Sony";
	        camera2.megapixel = 500;
	        camera2.display();
	    }



Once you create an object, you can access the properties and methods of the object using the dot(.) operator.



The main method is the program’s entry point, so it is always needed to see the result.
The new keyword can be used to create a new object, but it is unnecessary.


## Class and Objects in Dart


**What is class?**

Class is blueprint for object.

**What is object?**

Object is the instance of class.


Example:


	class SimpleInterest{
	  //properties of simple interest
	  double? principal;
	  double? rate;
	  double? time;
	  
	  //functions of simple interest
	  double interest(){
	    return (principal! * rate! * time!)/100;
	  }
	}
	void main(){
	  //object of simple interest created
	  SimpleInterest simpleInterest = SimpleInterest();
	  
	  //setting properties for simple interest
	  simpleInterest.principal=1000;
	  simpleInterest.rate=10;
	  simpleInterest.time=2;
	  
	  //functions of simple interest called
	  print("Simple Interest is ${simpleInterest.interest()}.");
	}


## Constructor In Dart

A constructor is a special method used to initialize an object. It is called automatically when an object is created, and it can be used to set the initial values for the object’s properties. 

Example:

	Person person = Person("John", 30)
	
If you don’t define a constructor for class, then you need to set the values of the properties manually.

	Person person = Person();
	person.name = "John";
	person.age = 30;
	
The constructor’s name should be the same as the class name.
Constructor doesn’t have any return type.

	class ClassName {
	  // Constructor declaration: Same as class name
	  ClassName() {
	    // body of the constructor
	  }
	}
	


*     The constructor’s name should be the same as the class name.
*     Constructor doesn’t have any return type.
*     Constructor is only called once at the time of the object creation.
*     Constructor is called automatically when an object is created.
*     Constructor is used to initialize the values of the properties of the class.

Example:

	  class Patient {
	  int? age;
	  String? disaese;
	 
	  // Constructor
	  Patient({this.age = 56, this.disaese = "bolest"});
	
	  // Method
	  void display() {
	    print("Age: ${this.age}");
	    print("Disaese: ${this.disaese}");
	  }
	}
	
	void main(){
	  Patient patient = Patient();
	  patient.display();
	}



## Default Constructor in Dart


The constructor which is automatically created by the dart compiler if you don’t create a constructor is called a default constructor. A default constructor has no parameters. A default constructor is declared using the class name followed by parentheses ().

Example:


	  class Person {
	  String? name;
	  String? planet;
	
	  // Default Constructor
	  Person() {
	    print(
	        "Constructor called"); // this is for checking the constructor is called or not.
	    planet = "Earth";
	  }
	}
	
	void main() {
	  // Here student is object of class Student.
	  Person person = Person();
	  person.name = "Srdjan";
	  print("Name: ${person.name}");
	  print("Planet: ${person.planet}");
	 
	}


## Parameterized Constructor in Dart


Parameterized constructor is used to initialize the instance variables of the class. Parameterized constructor is the constructor that takes parameters. It is used to pass the values to the constructor at the time of object creation.


Example:


    class Student {
      String? name;
      int? age;
    
      // Constructor
      Student({String? name = "John", int? age = 0}) {
        this.name = name;
        this.age = age;
      }
    }
    
    void main(){
        // Here student is object of class Student. 
        Student student = Student();
        print("Name: ${student.name}");
        print("Age: ${student.age}");
    }
    
## Named Constructor in Dart   


In most programming languages like java, c++, c#, etc., we can create multiple constructors with the same name. But in Dart, this is not possible. Well, there is a way. We can create multiple constructors with the same name using named constructors.



			class Car {
		  String? name;
		  String? color;
		  int? price;
		
		  // Default Constructor
		  Car() {
		    print("This is a default constructor");
		  }
		
		  // Named Constructor
		  Car.namedConstructor(String name, String color, int price) {
		    this.name = name;
		    this.color = color;
		    this.price = price;
		  }
		
		  // Named Constructor
		  Car.namedConstructor2(String name, String color) {
		    this.name = name;
		    this.color = color;
		  }
		}
		
		void main() {
		  // Here car is object of class Car.
		  Car car = Car.namedConstructor('Porche', 'red', 5000);
		  print("Name: ${car.name}");
		  print("Color: ${car.color}");
		  print("Price: ${car.price}");
		
		  Car car2 = Car.namedConstructor2("FIAT", "white");
		  print("Name: ${car2.name}");
		  print("Color: ${car2.color}");
		
		  display(car.name, car.color, car.price);
		}
		
		void display(name, color, price) {
		  print('From method:');
		  print("Name: ${name}");
		  print("Color: ${color}");
		  print("Price: ${price}");
		}
    
    
    
   
## Constant Constructor In Dart 

Constant constructor is a constructor that creates a constant object. A constant object is an object whose value cannot be changed. A constant constructor is declared using the keyword const.    
Constant Constructor is used to create a object whose value cannot be changed. It Improves the performance of the program.
Rules:

*     All properties of the class must be final.
*     It does not have any body.
*    Only class containing const constructor is initialized using the const keyword.
	




		class Car {
		  final String name;
		  final String model;
		  final int price;
		
		  const Car(this.name, this.model, this.price);
		}
		
		void main() {
		  
		  Car car = const Car("PORCHE", "Z80", 200);
		  print("The car name is: ${car.name}");
		  print("The car model is: ${car.model}");
		  print("The car price is: ${car.price}");
		}
	



    
## S.O.L.I.D.   


   **S - Single-responsiblity Principle**
   
   *In other words, every class should have only one
    responsibility.*
    
    
    
    
  **O - Open-closed Principle**
  
 *Software entities  should be open for extension, but closed
    for modification.*
    
 **L - Liskov Substitution Principle**
  
 *Functions that use pointers or references to base classes must 
  be able to use objects of derived classes without knowing it.*
    
 **I - Interface Segregation Principle**
  
  *The Interface segregation principle: Clients should not be forced to depend upon interfaces that they do not use.*
    
 **D - Dependency Inversion Principle**
  
  *Depend upon abstractions, [not] concretions.*
  
  link: [youtube](https://www.youtube.com/watch?v=A5Q5F7lCquQ)


 
