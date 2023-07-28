# MOST ASKED INTERVIEW QUESTIONS ON C++ OOPS

**1. What is Object-Oriented Programming (OOP)?**<br>
**Answer:** Object-Oriented Programming is a programming paradigm that organizes data and behavior into objects, which are instances of classes. It emphasizes the concepts of encapsulation, inheritance, polymorphism, and abstraction to design and model real-world systems.

**2. Explain the four fundamental principles of OOP.**<br>
**Answer:** The four fundamental principles of OOP are:
- Encapsulation: Bundling data and methods that operate on that data within a single unit (class).
- Inheritance: Allowing a class to inherit properties and behaviors from another class, promoting code reusability.
- Polymorphism: Providing a single interface to entities of different types, enabling flexibility in method implementation.
- Abstraction: Simplifying complex systems by hiding unnecessary details and showing only relevant functionality to the user.

**3. What is a class in C++?**<br>
**Answer:** A class in C++ is a user-defined data type that serves as a blueprint for creating objects. It encapsulates data members and member functions that define the characteristics and behavior of objects belonging to that class.

**4. Define an object in C++.**<br>
**Answer:** An object is an instance of a class. It is created using the class's constructor and represents a specific entity in the program, possessing its own unique set of data members and behaviors defined by the class.

**5. What is the difference between a class and an object?**<br>
**Answer:** A class is a blueprint or template that defines the structure and behavior of objects, while an object is an instance of that class created at runtime, having its own memory space and state.

**6. What is encapsulation? How is it achieved in C++?**<br>
**Answer:** Encapsulation is an OOP concept that restricts access to the internal state of an object, and it only allows operations through public methods. It hides the implementation details of an object, promoting better data security and code maintenance. Encapsulation in C++ is achieved by using access specifiers such as `public`, `private`, and `protected`.

**7. Describe the concept of inheritance and its types.**<br>
**Answer:** Inheritance is a mechanism in C++ where a class (derived class) can inherit properties and behaviors from another class (base class). It allows the derived class to reuse the code of the base class, promoting code reusability and extensibility. There are different types of inheritance: single, multiple, multilevel, and hierarchical inheritance.

**8. How does C++ support multiple inheritance?**<br>
**Answer:** C++ supports multiple inheritance, allowing a class to inherit from more than one base class. To handle ambiguity arising from multiple inherited members with the same name, C++ uses scope resolution (`::`) to specify which member to access.

**9. What is a constructor? Differentiate between a default constructor and a parameterized constructor.**<br>
**Answer:** A constructor is a special member function with the same name as the class that is automatically called when an object of that class is created. It is used to initialize the object's data members and allocate necessary resources.

A default constructor is one that can be called without any arguments and has no parameters. If a class has no constructor defined, the compiler generates a default constructor that initializes all the data members to default values (e.g., 0 for numeric types).

A parameterized constructor is one that takes parameters and allows custom initialization of data members based on provided values.

**10. What is a destructor? Why is it used?**<br>
**Answer:** A destructor is a special member function with the same name as the class but preceded by a tilde (`~`). It is automatically called when an object goes out of scope or is explicitly deleted using the `delete` operator. The destructor is used to release any resources held by the object, such as freeing allocated memory or closing files, ensuring proper cleanup.

**11. How do you create a copy constructor in C++?**<br>
**Answer:** A copy constructor is a constructor that creates a new object as a copy of an existing object. To create a copy constructor in C++, you define a constructor that takes a reference to the class type as its parameter and initializes the new object's data members using the values of the existing object.

Example:

```cpp
class MyClass {
public:
	// Copy constructor
	MyClass(const MyClass& other) {
		// Perform a deep copy of data members
	}
	// Rest of the class definition
};
```

**12. What is the purpose of the `this` pointer in C++?**<br>
**Answer:** The `this` pointer is a special pointer in C++ that points to the current object on which a member function is being called. It is used to differentiate between class data members and local variables that have the same name within a member function. The `this` pointer helps access the data members of the current object and is implicitly passed to non-static member functions.

**13. Explain the difference between `delete` and `delete[]`.**<br>
**Answer:** In C++, `delete` is used to deallocate memory that was dynamically allocated for a single object, while `delete[]` is used to deallocate memory that was dynamically allocated for an array of objects. It is essential to use the appropriate form depending on how memory was allocated using `new` and `new[]` to avoid undefined behavior and memory leaks.

**14. What is operator overloading in C++?**<br>
**Answer:** Operator overloading allows you to redefine the behavior of existing C++ operators (e.g., +, -, *, /) for user-defined classes. It enables you to use operators with custom-defined classes in a way that makes sense for the class's context.

**15. Provide an example of function overloading in C++.**<br>
**Answer:** Function overloading allows you to define multiple functions with the same name but different parameter lists. The appropriate function is called based on the arguments passed during the function call.

Example:

```cpp
class MathOperations {
public:
	int add(int a, int b) {
		return a + b;
	}
	  
	double add(double a, double b) {
		return a + b;
	}
};
```

**16. How is function overriding achieved in C++?**<br>
**Answer:** Function overriding is a feature of OOP that allows a derived class to provide a specific implementation for a method already defined in the base class. To achieve function overriding, the derived class redefines the base class's virtual function using the `virtual` keyword.

**17. What is a virtual function? How is it useful?**<br>
**Answer:** A virtual function is a member function of a class that is declared with the `virtual` keyword. It allows dynamic binding at runtime, meaning the appropriate function implementation is selected based on the actual object type (late binding) rather than the pointer or reference type (early binding). Virtual functions enable polymorphism in C++, allowing derived classes to have their specific implementations of a method.

**18. Define a pure virtual function. What is its significance?**<br>
**Answer:** A pure virtual function is a virtual function that has no implementation in the base class, declared with `= 0`. A class containing one or more pure virtual functions becomes an abstract class, and objects cannot be created from it. The significance of pure virtual functions lies in their ability to define an interface that derived classes must implement. By doing so, they enforce a contract between the base class and derived classes, ensuring that specific methods are implemented in each derived class.

**19. What are abstract classes and abstract methods in C++?**<br>
**Answer:** An abstract class is a class that contains one or more pure virtual functions. It cannot be instantiated, meaning objects cannot be created directly from an abstract class. Abstract classes serve as base classes, defining a common interface that derived classes must implement. Abstract methods are pure virtual functions declared within an abstract class.

**20. How can you prevent a class from being instantiated in C++?**<br>
**Answer:** To prevent a class from being instantiated in C++, you can make the class abstract by including at least one pure virtual function. This way, objects cannot be created directly from the class. Additionally, you can make the class constructor private, which prevents users from creating objects outside of the class's member functions. In this case, you can provide a static member function within the class to return an instance of the class (often called a "singleton" pattern).

**21. Explain the concept of friend functions in C++?**<br>
**Answer:** Friend functions in C++ are non-member functions that have access to the private and protected members of a class. They are declared as friends of the class using the `friend` keyword. Friend functions are useful when you need to allow external functions or classes to access the private members of a class without making them members of that class.

**22. What is the role of the `static` keyword in C++?**<br>
**Answer:** The `static` keyword in C++ has multiple meanings depending on the context:

- When used with class data members, it makes the data member shared among all objects of the class, meaning there is only one copy of the data for all instances of the class.

- When used with class member functions, it makes the function independent of any specific object of the class, allowing it to be called using the class name.

**23. How is memory allocated for objects in C++?**<br>
**Answer:** Memory for objects in C++ is allocated in two ways:

- Stack allocation: Objects with automatic storage duration are allocated on the stack. They are automatically deallocated when they go out of scope.

- Heap allocation: Objects with dynamic storage duration are allocated on the heap using `new` operator. They must be explicitly deallocated using `delete` to avoid memory leaks.

**24. Describe the difference between shallow copy and deep copy.**<br>
**Answer:** Shallow copy and deep copy are ways of copying objects in C++:

- Shallow copy: It copies the values of data members from one object to another, including any pointer values. Both objects will point to the same memory locations, which may lead to issues when deallocating memory.

- Deep copy: It creates a new copy of the entire object, including dynamically allocated memory. Each object has its memory, and changes in one object do not affect the other.

**25. What are smart pointers in C++? Provide examples.**<br>
**Answer:** Smart pointers are objects that behave like pointers but provide automatic memory management. They ensure proper deallocation of memory when objects are no longer needed, preventing memory leaks. C++ provides three types of smart pointers: `std::unique_ptr`, `std::shared_ptr`, and `std::weak_ptr`.

Example:

```cpp
#include <memory>
  
int main() {
	// std::unique_ptr
	std::unique_ptr<int> ptr = std::make_unique<int>(10);
	  
	// std::shared_ptr
	std::shared_ptr<int> sharedPtr = std::make_shared<int>(20);
	std::shared_ptr<int> sharedPtr2 = sharedPtr; // Reference count increased
	  
	// std::weak_ptr
	std::weak_ptr<int> weakPtr = sharedPtr; // Does not increase reference count
}
```

**26. How are namespaces used in C++?**<br>
**Answer:** Namespaces in C++ are used to avoid naming conflicts by enclosing identifiers within a named scope. They help organize code and make it more modular. To use a namespace, you either prefix the identifier with the namespace name followed by `::` or use the `using` directive to bring specific names into the current scope.

**27. Explain the purpose of the `const` keyword in C++?**<br>
**Answer:** The `const` keyword in C++ is used to indicate that an object or a function parameter is constant and cannot be modified. It ensures that the value of the object remains unchanged and helps prevent accidental modifications.

**28. What are access specifiers? Provide their significance.**<br>
**Answer:** Access specifiers (`public`, `private`, and `protected`) in C++ control the visibility and accessibility of class members:
- `public`: Members with public access specifier are accessible from anywhere, including outside the class.
- `private`: Members with private access specifier are only accessible within the class, and not from outside.
- `protected`: Members with protected access specifier are accessible within the class and its derived classes.

Access specifiers provide encapsulation and data hiding, allowing you to control the accessibility of class members.

**29. How do you handle exceptions in C++ using `try`, `catch`, and `throw`?**<br>
**Answer:** Exception handling in C++ allows you to handle runtime errors gracefully. You use `try` to enclose the code that might throw an exception, `catch` to handle the exception, and `throw` to throw an exception when an error occurs.

Example:

```cpp
#include <iostream>
  
int divide(int a, int b) {
	if (b == 0)
		throw std::runtime_error("Division by zero");
	return a / b;
}
  
int main() {
	try {
		int result = divide(10, 2);
		std::cout << "Result: " << result << std::endl;
	} catch (const std::exception& e) {
		std::cerr << "Exception caught: " << e.what() << std::endl;
	}
}
```

**30. Discuss the differences between `std::vector` and C-style arrays.**<br>
**Answer:** `std::vector` is a dynamic array-like container from the C++ Standard Library, while C-style arrays are fixed-size arrays with no built-in memory management. Some differences between them are:
- `std::vector` can dynamically resize, whereas C-style arrays have a fixed size determined at compile time.
- `std::vector` provides member functions to get the size and capacity, while C-style arrays do not store their size explicitly.
- `std::vector` can be passed as a function argument without decay to a pointer, unlike C-style arrays.
- `std::vector` is part of the C++ Standard Library and provides various useful member functions.
  
**31. Explain the use of the `const` member function in C++?**<br>
**Answer:** A `const` member function is a member function of a class that is marked as `const`. It promises not to modify the state of the object it is called on. A `const` member function can be called on `const` objects and can read but cannot modify the data members of the object.

Example:

```cpp
class MyClass {
public:
	void modifyData() { /* Modify data members */ }
	void readData() const { /* Read data members but not modify */ }
};
  
int main() {
	const MyClass obj1; // Const object
	obj1.readData(); // Allowed
	// obj1.modifyData(); // Not allowed, will result in a compilation error
	return 0;
}
```

**32. What is the role of the `mutable` keyword in C++?**<br>
**Answer:** The `mutable` keyword is used to indicate that a data member of a class can be modified even in a `const` member function. It allows specific data members to be modified within `const` member functions without violating the `const` contract of the function.

Example:

```cpp
class MyClass {
public:
	mutable int counter = 0; // Mutable data member
	  
	void incrementCounter() const {
		counter++; // Allowed because counter is mutable
	}
};
```

**33. How do you implement operator overloading for a user-defined class?**<br>
**Answer:** Operator overloading for a user-defined class is achieved by defining the operator function as a member function or a global function. The operator function's name follows the format `operator<symbol>`, where `<symbol>` is the symbol of the operator to be overloaded.

Example (overloading the `+` operator):

```cpp
class Complex {
public:
	int real;
	int imag;
	  
	Complex operator+(const Complex& other) {
		Complex result;
		result.real = this->real + other.real;
		result.imag = this->imag + other.imag;
		return result;
	}
};
```

**34. What is a friend class in C++?**<br>
**Answer:** A friend class in C++ is a class that is granted access to the private and protected members of another class. It is declared as a friend within the class that wants to provide access. Friend classes can access private members as if they were their own members.

**35. Describe the process of dynamic casting in C++?**<br>
**Answer:** Dynamic casting is a type of C++ casting used to convert a pointer or reference of a base class to a pointer or reference of a derived class at runtime. It allows you to check if the conversion is valid before performing it. If the conversion is not possible, dynamic casting returns a null pointer for pointers or throws a `std::bad_cast` exception for references.

Example:

```cpp
class Base {
	// Base class definition
};
  
class Derived : public Base {
	// Derived class definition
};
  
int main() {
	Base* basePtr = new Derived;
	Derived* derivedPtr = dynamic_cast<Derived*>(basePtr);
	  
	if (derivedPtr != nullptr) {
		// Conversion successful
		// Use derivedPtr to access Derived class members
	} else {
		// Conversion failed
	}
	  
	delete basePtr;
	return 0;
}
```

**36. What are the differences between `static_cast`, `dynamic_cast`, `const_cast`, and `reinterpret_cast`?**<br>
**Answer:** The different C++ casts are used for different purposes:
- `static_cast`: Used for basic type conversions, upcasting (derived to base), and non-polymorphic type conversions.
- `dynamic_cast`: Used for safe downcasting (base to derived) with polymorphic classes. Returns a null pointer if the conversion is not valid.
- `const_cast`: Used to add or remove `const` or `volatile` qualifiers from a variable.
- `reinterpret_cast`: Used to perform low-level reinterpretation of the pointer or reference type, such as converting a pointer to an unrelated type.

**37. What are virtual destructors? Why are they important?**<br>
**Answer:** A virtual destructor is a destructor declared with the `virtual` keyword in the base class. When a derived class object is deleted through a pointer to the base class, a virtual destructor ensures that the proper destructors of both the base and derived classes are called in the correct order, preventing memory leaks.

Example:

```cpp
class Base {
public:
	virtual ~Base() {
		// Virtual destructor
	}
};
  
class Derived : public Base {
public:
	~Derived() {
		// Derived class destructor
	}
};
  
int main() {
	Base* ptr = new Derived;
	delete ptr; // Calls both Base and Derived destructors
	return 0;
}
```

**38. Discuss the concept of a template in C++?**<br>
**Answer:** A template in C++ is a powerful feature that allows you to write generic classes and functions that work with different data types. It enables you to define a class or function with placeholders for type(s) or value(s), allowing you to create a wide range of data structures and algorithms that are reusable and type-safe.

**39. What are the advantages of using templates in C++?**<br>
**Answer:** Using templates in C++ offers several advantages:
- Code Reusability: Templates allow you to create generic classes and functions that can work with multiple data types, reducing code duplication.
- Type Safety: Templates are type-safe, as the compiler enforces type correctness at compile-time.
- Performance: Templates use compile-time polymorphism (generating specialized code for each data type), leading to efficient code execution.
- Standard Library Support: C++ Standard Library containers, such as `std::vector` and `std::map`, use templates to provide flexible data structures.

**40. How can you handle memory leaks in C++?**<br>
**Answer:** To handle memory leaks in C++, you should ensure that every dynamically allocated object using `new` is properly deallocated using `delete`. You can use smart pointers like `std::unique_ptr` or `std::shared_ptr` to manage memory automatically. Alternatively, consider using standard library containers (`std::vector`, `std::string`, etc.), which handle memory management for you.

**41. Explain the concept of RAII (Resource Acquisition Is Initialization) in C++?**<br>
**Answer:** RAII is a C++ programming technique that ties the lifetime of a resource (like memory, file handle, or mutex) to the lifetime of an object. When the object goes out of scope, its destructor is called, and it automatically releases the resource. RAII ensures that resources are correctly acquired and released, preventing resource leaks and improving code safety.

**42. What is the difference between a class template and a function template?**<br>
**Answer:** A class template in C++ defines a blueprint for a generic class that can work with different data types. It allows you to create a family of classes with similar functionalities, but each instantiation has its own set of data members and functions.

A function template, on the other hand, defines a generic function that can operate on multiple data types. It allows you to define a single function that can handle various types of parameters without writing separate functions for each data type.

**43. Describe the role of the `explicit` keyword in C++?**<br>
**Answer:** The `explicit` keyword is used to prevent implicit conversions that the compiler would normally perform. It can be applied to constructors to disallow implicit conversion from the constructor's argument type to the class type. By doing so, you force users to perform explicit conversions (using constructor syntax) when creating objects.

**44. What is the `volatile` keyword used for in C++?**<br>
**Answer:** The `volatile` keyword in C++ is a type qualifier used to indicate that a variable's value may change at any time outside the control of the program (e.g., by hardware or other threads). It tells the compiler not to perform certain optimizations that could assume the variable's value remains constant.

**45. How can you prevent inheritance in C++?**<br>
**Answer:** To prevent inheritance in C++, you can declare the base class constructor as private or delete it. This way, other classes cannot derive from it. Additionally, you can make the class `final`, which indicates that it cannot be used as a base class for other classes.

Example:

```cpp
class Base final {
private:
	Base() {} // Prevent inheritance by making the constructor private
	friend class FriendClass; // Allow FriendClass to access Base's members
};
```

**46. Discuss the differences between `new` and `malloc`.**<br>
**Answer:** `new` and `malloc` are used to dynamically allocate memory in C++:
- `new`: A C++ operator that not only allocates memory but also calls the constructor to initialize the object if it is a class type. It returns a pointer to the allocated memory.
- `malloc`: A C function from C's standard library that allocates a block of memory of the specified size. It does not call the constructor for class objects and returns a void pointer (`void*`).

In C++, it is generally recommended to use `new` for dynamic memory allocation, especially when dealing with objects, as it automatically handles constructor calls and type safety.

**47. How are private and protected inheritance different from public inheritance?**<br>
**Answer:** In C++, there are three types of inheritance:
- Public inheritance: Derived class inherits all the public and protected members of the base class as public and protected, respectively.
- Protected inheritance: Derived class inherits all the public and protected members of the base class as protected.
- Private inheritance: Derived class inherits all the public and protected members of the base class as private.

The main difference lies in the accessibility of inherited members in the derived class. Public inheritance preserves the accessibility, while protected and private inheritance restrict access to the inherited members.

**48. Explain the diamond problem in the context of multiple inheritance.**<br>
**Answer:** The diamond problem is an ambiguity that can occur in multiple inheritance when a class inherits from two or more classes, which in turn share a common base class. If the derived class does not explicitly resolve the ambiguity, it can lead to ambiguity in accessing the members of the common base class.

Example:

```cpp
class A {
public:
	void foo() { /* Do something */ }
};
  
class B : public A {};
class C : public A {};
  
class D : public B, public C {
	// Ambiguity in calling foo() without explicit resolution
};
```

**49. What are lambda expressions in C++? Provide an example.**<br>
**Answer:** Lambda expressions are anonymous functions introduced in C++11. They allow you to define inline functions without needing to declare a separate function or functor. Lambdas are commonly used with standard algorithms and as callback functions.

Example:

```cpp
#include <iostream>
  
int main() {
	int x = 5;
	int y = 10;
	  
	// Lambda expression taking two integers and returning their sum
	auto sum = [](int a, int b) { return a + b; };
	  
	int result = sum(x, y);
	std::cout << "Sum: " << result << std::endl;
	return 0;
}
```

**50. Describe the use of `std::move` and move constructors/move assignment operators.**<br>
**Answer:** `std::move` is a utility function from the C++ Standard Library that converts an lvalue (an object with a name) into an rvalue (allows moving resources instead of copying). Move constructors and move assignment operators are special member functions used to perform efficient transfers of resources (e.g., memory) from one object to another.

Move semantics, enabled by move constructors and move assignment operators, are especially useful when dealing with dynamically allocated resources or large objects to avoid unnecessary deep copies.
