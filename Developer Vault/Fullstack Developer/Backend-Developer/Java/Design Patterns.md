#BackendDeveloper  #Java-Concepts 

Design patterns are reusable solutions to common software design problems, providing best practices to solve recurring issues in a structured and efficient manner.

Familiarity with common design patterns such as Singleton, Factory, Builder, Strategy, Observer, and Decorator.
- **Singleton**: Ensures a class has only one instance and provides a global point of access to it.
    
- **Factory**: Defines an interface for creating an object but lets subclasses alter the type of objects that will be created.
    
- **Builder**: Separates the construction of a complex object from its representation, allowing the same construction process to create different representations.
    
- **Strategy**: Defines a family of algorithms, encapsulates each one, and makes them interchangeable to let the algorithm vary independently from clients that use it.
    
    - Creates an interface and that is used on various classes.
    
    ```java
    public class Main {
        public static void main(String[] args) {
            ShoppingCart cart = new ShoppingCart();
    
            // Paying with Credit Card
            cart.setPaymentStrategy(new CreditCardPayment("1234567890123456", "John Doe", "123", "12/24"));
            cart.checkout(100);
            // Paying with PayPal
            cart.setPaymentStrategy(new PayPalPayment("john.doe@example.com", "password123"));
            cart.checkout(200);
        }
    }
    ```
    
- **Observer**: Allows an object to notify other objects about changes in its state, facilitating a one-to-many dependency between objects.
    
- **Decorator**: Adds additional responsibilities to an object dynamically, providing a flexible alternative to subclassing for extending functionality.