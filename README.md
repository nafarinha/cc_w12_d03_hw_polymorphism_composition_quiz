# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

   > The ability to apear in multiple (*poly*-) different forms (*-morphism*).

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

   > In OOP, polymorphism allows  a single action to be performed in different ways.
   >
   > ```Java	
   > public abstract class Car{
   >   ...
   >     public abstract void startEngine();
   > } 
   > ```

   > ```java
   > public class electricCar extends Car{
   >   ...
   >     public void startEngine() {
   >     	System.out.println("zzzzzz");
   >   }
   > }
   > ```

   > ```java
   > public class ICECar extends Car {
   >   ...
   >     public void startEngine() {
   >     	System.out.println("vrummmmmmm");
   >   }
   > }
   > ```
   >
   > 

3. What can we use to implement polymorphism in Java?

   > Abstract classes or Interfaces.

4. How many 'forms' can an object take when using polymorphism?

   > An object using polymorphism can take the 'form' aka use its inherited behaviours from its super-class or override the inherited behaviours to perform specifc actions.

5. Give an example of when you could use polymorphism.

   > Different classes may share a similar behaviour implemented by an Interface method. Despite this, each class has a different method body to reflect its own specific action. All output devices can have an `output()`method. In a printer class this method would return a printed page while in a monitor class it would return a number of  pixels.



# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?

   > Composition in OOP is the ability for a class to reference one or more different classes in its instance variables.

7. When would you use composition? Provide a simple example in Java.

   > To represent a *has-a* association between two classes. A Car *has* a Engine, it *is* not an Engine.
   >
   > ```java
   > public class Engine {
   >   private int cylinders;
   >   private String fuel;
   >   private int powerInKW;
   >   
   >   public Engine(int cylinders, String fuel, int powerInKW) {
   >     this.cylinders = cylinders;
   >     this.fuel = fuel;
   >     this.powerInKw = powerInKw;
   >   }
   > }
   > ```
   >
   > 
   >
   > ```java
   > public class Car {
   >   private String make;
   >   private String model;
   >   private Engine engine;
   >   
   >   public Car (String make, String model, Engine engine) {
   >     this.make = make;
   >     this.model = model;
   >     this.engine = engine;
   >   }
   > }
   > ```
   >
   > 

8. What is/are the advantage(s) of using composition?

   > Reinforces encapsulation, easier-to-maintain and reusable code. 

9. When an object is destroyed, what happens to all the objects it is composed of?

   > The objects that used to compose a destroyed object are also destroyed. 