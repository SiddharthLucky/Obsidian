#BackendDeveloper  #Java-Concepts 

Java enable type-safe code by allowing classes, interfaces, and methods to operate on specified data types while providing compile-time type checking.

- **Generics Basics**: Generics enable type-safe code and eliminate the need for casting by allowing classes, interfaces, and methods to operate on specific data types.
- **Type Parameters**: Type parameters are placeholders for types, specified within angle brackets (**`<>`**), and can be used to enforce type safety.
- **Bounded Type Parameters**: Bounded type parameters restrict the types that can be used as arguments by specifying an upper or lower bound (e.g., **`<T extends Number>`**).
- **Wildcards**: Wildcards (**`?`**) represent an unknown type and can be bounded with **`extends`** (upper bound) or **`super`** (lower bound) to increase flexibility.
- **Generic Methods**: Generic methods define type parameters in the method signature to enable type-safe operations within the method.
- **Type Erasure**: Type erasure is the process by which generic type information is removed at runtime, ensuring compatibility with legacy code.
- **Generic Classes and Interfaces**: Generic classes and interfaces use type parameters to create classes and interfaces that can operate on different data types without sacrificing type safety.
- **Raw Types**: Raw types refer to the use of generic types without specifying type parameters, which can lead to unchecked warnings and potential runtime errors.
- **Type Inference**: Type inference allows the compiler to determine the type parameters automatically based on the context, reducing verbosity in code.
    - **Interview questions on Generics:**
        
        1. **What are generics in Java, and why are they used?** ◦ Generics enable type-safe code by allowing classes, interfaces, and methods to operate on specified data types, reducing runtime errors and the need for casting.
        2. **Explain the concept of type parameters in generics.** ◦ Type parameters are placeholders for types specified within angle brackets (**`<>`**), allowing for type-safe operations and reusable code.
        3. **What are bounded type parameters, and how are they useful?** ◦ Bounded type parameters restrict the types that can be used as arguments by specifying an upper or lower bound, enabling more precise type constraints and ensuring compatibility with specific type hierarchies.
        4. **How do wildcards work in generics, and what are their types?** ◦ Wildcards (**`?`**) represent an unknown type and can be bounded with **`extends`** (upper bound) or **`super`** (lower bound) to provide flexibility in using generic types while maintaining some type safety.
        5. **What is type erasure, and how does it affect generics in Java?** ◦ Type erasure is the process by which generic type information is removed at runtime, ensuring compatibility with legacy code but limiting the ability to use type-specific information at runtime.
        6. **Can you explain the difference between a generic class and a raw type?** ◦ A generic class uses type parameters to operate on specified data types safely, while a raw type omits type parameters, leading to unchecked warnings and potential runtime errors.
        7. **What is type inference, and how does it simplify the use of generics?** ◦ Type inference allows the compiler to automatically determine type parameters based on the context, reducing verbosity and making the code cleaner and easier to read.
        8. **Give an example of a generic method.**
        
        ```java
        public <T> void printArray(T[] array) {
            for (T element : array) {
                System.out.println(element);
            }
        }
        ```
        
        ```
          ◦ This method uses a type parameter **`<T>`** to allow for printing arrays of any type.
        ```
        
        9. **What are the limitations of generics in Java?** ◦ Generics cannot be used with primitive types directly, type information is erased at runtime, and creating instances of generic type parameters or using static fields of type parameters is not allowed.
        10. **Why is it important to avoid using raw types?** ◦ Using raw types bypasses type checking, leading to potential **`ClassCastException`** at runtime and reducing code readability and maintainability.