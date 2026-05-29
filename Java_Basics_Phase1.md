# 🚀 Complete Java Mastery Guide: Beginner to Advanced for Automation Testing

---

## 📋 TABLE OF CONTENTS

1. **Phase 1: Java Foundations (Weeks 1-4)**
2. **Phase 2: Object-Oriented Programming (Weeks 5-8)**
3. **Phase 3: Intermediate Java (Weeks 9-12)**
4. **Phase 4: Advanced Java (Weeks 13-16)**
5. **Phase 5: Automation Testing Foundations (Weeks 17-20)**
6. **Phase 6: Advanced Automation (Weeks 21-24)**

---

---

# 📘 PHASE 1: JAVA FOUNDATIONS (Weeks 1-4)

---

## Chapter 1: What is Java?

### Theory:
Java is a **high-level, object-oriented programming language** developed by James Gosling at Sun Microsystems in 1995 (now owned by Oracle). Java follows the principle of **"Write Once, Run Anywhere" (WORA)**, meaning code written on one platform can run on any platform that has a Java Virtual Machine (JVM).

### How Java Works:
```
[Your Code (.java)] 
      ↓ (Compilation)
[Bytecode (.class)] 
      ↓ (JVM Interprets)
[Machine Code] 
      ↓
[Computer Executes]
```

### Key Components:
- **JDK (Java Development Kit):** The complete development package (includes JRE + development tools)
- **JRE (Java Runtime Environment):** The environment to run Java programs (includes JVM + libraries)
- **JVM (Java Virtual Machine):** The engine that actually runs your bytecode

### Why Java for Automation Testing?
1. Most automation tools (Selenium, Appium) have strongest support for Java
2. Huge community and library ecosystem
3. Platform independence
4. Strong typing helps catch bugs early
5. Most job postings for SDET require Java

---

## Chapter 2: Setting Up Your Environment

### Step 1: Install JDK
```
1. Go to https://www.oracle.com/java/technologies/downloads/
2. Download JDK 17 or later (LTS version)
3. Install it
4. Set JAVA_HOME environment variable
5. Add Java to your PATH
```

### Step 2: Verify Installation
```bash
# Open terminal/command prompt
java -version
javac -version
```

### Step 3: Install IDE (IntelliJ IDEA recommended)
```
1. Go to https://www.jetbrains.com/idea/
2. Download Community Edition (Free)
3. Install and configure
```

---

## Chapter 3: Your First Java Program

### Theory:
Every Java program needs at least one **class** and a **main method**. The main method is the entry point where the program starts executing.

```java
// This is your first Java program
// File name: HelloWorld.java

public class HelloWorld {
    // main method - entry point of the program
    public static void main(String[] args) {
        System.out.println("Hello, World!");
        System.out.println("I am learning Java for Automation Testing!");
    }
}
```

### Breaking Down Every Word:

| Keyword | Meaning |
|---------|---------|
| `public` | Access modifier - anyone can access this |
| `class` | Blueprint for creating objects |
| `HelloWorld` | Name of the class (must match filename) |
| `static` | Belongs to the class, not an object instance |
| `void` | This method doesn't return any value |
| `main` | Special method name - JVM looks for this |
| `String[] args` | Array of strings - command line arguments |
| `System.out.println()` | Prints text to the console |

### Rules to Remember:
```java
// 1. File name MUST match the public class name
// 2. Java is CASE-SENSITIVE (Hello ≠ hello)
// 3. Every statement ends with a semicolon ;
// 4. Code blocks are enclosed in curly braces { }
// 5. The main method signature must be exact
```

---

## Chapter 4: Variables and Data Types

### Theory:
A **variable** is a container that holds data in memory. Think of it as a labeled box where you store a value. Every variable in Java must have a **data type** which tells the computer what kind of data it will hold and how much memory to allocate.

### Primitive Data Types (8 types):

```java
public class DataTypes {
    public static void main(String[] args) {
        
        // ============ INTEGER TYPES ============
        
        // byte: 1 byte, range: -128 to 127
        // Use when: saving memory with small numbers
        byte myAge = 25;
        
        // short: 2 bytes, range: -32,768 to 32,767
        // Use when: slightly larger small numbers
        short temperature = -200;
        
        // int: 4 bytes, range: -2.1 billion to 2.1 billion
        // Use when: DEFAULT choice for whole numbers
        int salary = 50000;
        int population = 1400000000;
        
        // long: 8 bytes, range: very large numbers
        // Use when: numbers bigger than int range
        // NOTE: must add 'L' at the end
        long worldPopulation = 7800000000L;
        long distanceToSun = 149600000000L;
        
        // ============ DECIMAL TYPES ============
        
        // float: 4 bytes, ~6-7 decimal digits precision
        // NOTE: must add 'f' at the end
        float pi = 3.14f;
        float price = 99.99f;
        
        // double: 8 bytes, ~15 decimal digits precision  
        // Use when: DEFAULT choice for decimals
        double precisePI = 3.141592653589793;
        double accountBalance = 1234567.89;
        
        // ============ OTHER TYPES ============
        
        // char: 2 bytes, single character
        // Use single quotes ''
        char grade = 'A';
        char symbol = '@';
        char digit = '7';  // This is a character, not a number!
        
        // boolean: 1 bit, true or false only
        // Use when: yes/no, on/off, true/false decisions
        boolean isTestPassed = true;
        boolean isLoggedIn = false;
        boolean hasPermission = true;
        
        // ============ PRINTING VARIABLES ============
        
        System.out.println("My age: " + myAge);
        System.out.println("Salary: $" + salary);
        System.out.println("PI value: " + precisePI);
        System.out.println("Grade: " + grade);
        System.out.println("Test Passed: " + isTestPassed);
    }
}
```

### Memory Visualization:
```
Variable Name    Type      Memory    Value
─────────────────────────────────────────
myAge            byte      1 byte    25
salary           int       4 bytes   50000
precisePI        double    8 bytes   3.14159...
grade            char      2 bytes   'A'
isTestPassed     boolean   1 bit     true
```

### Non-Primitive (Reference) Types:

```java
public class ReferenceTypes {
    public static void main(String[] args) {
        
        // String: sequence of characters (text)
        // Use double quotes ""
        String name = "John Doe";
        String company = "Google";
        String testCaseName = "Verify Login Functionality";
        
        // Key difference from primitive:
        // - Stored in heap memory
        // - Can be null (no value)
        // - Have methods (built-in functions)
        
        String nullExample = null;  // No value assigned
        
        System.out.println("Name: " + name);
        System.out.println("Length of name: " + name.length());
        System.out.println("Uppercase: " + name.toUpperCase());
    }
}
```

### Variable Naming Rules & Conventions:

```java
public class NamingConventions {
    public static void main(String[] args) {
        
        // ✅ VALID variable names
        int age = 25;
        int _count = 10;           // can start with underscore
        int $amount = 100;         // can start with dollar sign
        int myVariableName = 5;    // camelCase (RECOMMENDED)
        int student1Age = 20;      // can contain numbers (not at start)
        
        // ❌ INVALID variable names
        // int 1stNumber = 10;     // Cannot start with a number
        // int my-name = "John";   // Cannot use hyphens
        // int my name = "John";   // Cannot have spaces
        // int class = 5;          // Cannot use reserved keywords
        
        // 📌 CONVENTIONS (not rules, but best practices):
        // - Variables: camelCase → firstName, testResult
        // - Constants: ALL_CAPS → MAX_RETRY, BASE_URL
        // - Classes: PascalCase → LoginPage, TestRunner
        // - Methods: camelCase → clickButton(), verifyTitle()
        
        // Constants (values that never change)
        final int MAX_RETRY_COUNT = 3;
        final String BASE_URL = "https://www.google.com";
        // MAX_RETRY_COUNT = 5;  // ❌ ERROR! Cannot change a final variable
    }
}
```

---

## Chapter 5: Operators

### Theory:
Operators are special symbols that perform operations on variables and values. Think of them as the verbs of programming - they DO things with your data.

```java
public class Operators {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // 1. ARITHMETIC OPERATORS (Math operations)
        // ═══════════════════════════════════════
        
        int a = 20;
        int b = 7;
        
        System.out.println("=== Arithmetic Operators ===");
        System.out.println("a + b = " + (a + b));   // Addition: 27
        System.out.println("a - b = " + (a - b));   // Subtraction: 13
        System.out.println("a * b = " + (a * b));   // Multiplication: 140
        System.out.println("a / b = " + (a / b));   // Division: 2 (integer division!)
        System.out.println("a % b = " + (a % b));   // Modulus (remainder): 6
        
        // ⚠️ IMPORTANT: Integer division truncates decimals
        System.out.println("20 / 7 = " + (20 / 7));       // Output: 2 (not 2.857!)
        System.out.println("20.0 / 7 = " + (20.0 / 7));   // Output: 2.857... (correct!)
        
        
        // ═══════════════════════════════════════
        // 2. ASSIGNMENT OPERATORS (Assign values)
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Assignment Operators ===");
        int x = 10;          // Simple assignment
        
        x += 5;              // x = x + 5 → 15
        System.out.println("x += 5: " + x);
        
        x -= 3;              // x = x - 3 → 12
        System.out.println("x -= 3: " + x);
        
        x *= 2;              // x = x * 2 → 24
        System.out.println("x *= 2: " + x);
        
        x /= 4;              // x = x / 4 → 6
        System.out.println("x /= 4: " + x);
        
        x %= 4;              // x = x % 4 → 2
        System.out.println("x %= 4: " + x);
        
        
        // ═══════════════════════════════════════
        // 3. INCREMENT / DECREMENT OPERATORS
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Increment/Decrement ===");
        int count = 10;
        
        count++;              // Post-increment: use then increase
        System.out.println("count++: " + count);    // 11
        
        ++count;              // Pre-increment: increase then use
        System.out.println("++count: " + count);    // 12
        
        count--;              // Post-decrement
        System.out.println("count--: " + count);    // 11
        
        // The difference matters in expressions:
        int val = 5;
        System.out.println("val++: " + val++);  // Prints 5, THEN val becomes 6
        System.out.println("val now: " + val);   // Prints 6
        System.out.println("++val: " + ++val);   // val becomes 7, THEN prints 7
        
        
        // ═══════════════════════════════════════
        // 4. COMPARISON/RELATIONAL OPERATORS
        // (Return true or false - essential for testing!)
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Comparison Operators ===");
        int p = 10, q = 20;
        
        System.out.println("p == q: " + (p == q));   // Equal to: false
        System.out.println("p != q: " + (p != q));   // Not equal to: true
        System.out.println("p > q: " + (p > q));     // Greater than: false
        System.out.println("p < q: " + (p < q));     // Less than: true
        System.out.println("p >= q: " + (p >= q));    // Greater or equal: false
        System.out.println("p <= q: " + (p <= q));    // Less or equal: true
        
        
        // ═══════════════════════════════════════
        // 5. LOGICAL OPERATORS 
        // (Combine multiple conditions - VERY important for testing!)
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Logical Operators ===");
        boolean isAdult = true;
        boolean hasLicense = false;
        
        // AND (&&): Both must be true
        System.out.println("Can drive? " + (isAdult && hasLicense));  // false
        
        // OR (||): At least one must be true
        System.out.println("Has any qualification? " + (isAdult || hasLicense));  // true
        
        // NOT (!): Reverses the boolean
        System.out.println("Is not adult? " + (!isAdult));  // false
        
        // Practical testing example:
        boolean isElementVisible = true;
        boolean isElementEnabled = true;
        boolean isElementClickable = isElementVisible && isElementEnabled;
        System.out.println("Can click element? " + isElementClickable);  // true
        
        
        // ═══════════════════════════════════════
        // 6. TERNARY OPERATOR (Shorthand if-else)
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Ternary Operator ===");
        int score = 75;
        // Syntax: condition ? valueIfTrue : valueIfFalse
        String result = (score >= 60) ? "PASS" : "FAIL";
        System.out.println("Result: " + result);  // PASS
        
        String status = (score >= 90) ? "Excellent" : 
                         (score >= 70) ? "Good" : 
                         (score >= 60) ? "Average" : "Poor";
        System.out.println("Status: " + status);  // Good
    }
}
```

---

## Chapter 6: Type Casting

### Theory:
Type casting is converting one data type to another. It's like pouring water from a small glass into a big glass (easy/automatic) vs. pouring from a big glass into a small glass (risky, might spill - needs explicit permission).

```java
public class TypeCasting {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // WIDENING (Automatic/Implicit) - Small → Big
        // byte → short → int → long → float → double
        // ═══════════════════════════════════════
        
        int myInt = 100;
        long myLong = myInt;       // Automatic: int → long
        float myFloat = myLong;    // Automatic: long → float
        double myDouble = myFloat; // Automatic: float → double
        
        System.out.println("int: " + myInt);         // 100
        System.out.println("long: " + myLong);       // 100
        System.out.println("float: " + myFloat);     // 100.0
        System.out.println("double: " + myDouble);   // 100.0
        
        // ═══════════════════════════════════════
        // NARROWING (Manual/Explicit) - Big → Small
        // double → float → long → int → short → byte
        // ⚠️ Risk of data loss!
        // ═══════════════════════════════════════
        
        double bigDouble = 9.78;
        int smallInt = (int) bigDouble;  // Must explicitly cast
        
        System.out.println("double: " + bigDouble);   // 9.78
        System.out.println("int: " + smallInt);        // 9 (decimal part lost!)
        
        // String to Number conversions (very common in testing!)
        String ageString = "25";
        int age = Integer.parseInt(ageString);         // String → int
        double price = Double.parseDouble("99.99");    // String → double
        
        // Number to String
        String numStr = String.valueOf(42);            // int → String
        String numStr2 = Integer.toString(42);         // Alternative way
        String numStr3 = "" + 42;                      // Concatenation trick
    }
}
```

---

## Chapter 7: Taking User Input

### Theory:
The `Scanner` class allows your program to read input from the user via the console. In testing, you'll often read data from files, but understanding Scanner helps with basic input concepts.

```java
import java.util.Scanner;  // Must import this!

public class UserInput {
    public static void main(String[] args) {
        
        // Create a Scanner object to read from keyboard
        Scanner scanner = new Scanner(System.in);
        
        // Reading different types of input
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();  // Reads entire line
        
        System.out.print("Enter your age: ");
        int age = scanner.nextInt();       // Reads an integer
        
        System.out.print("Enter your salary: ");
        double salary = scanner.nextDouble();  // Reads a double
        
        // Display the information
        System.out.println("\n=== Your Details ===");
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Salary: $" + salary);
        
        // ⚠️ COMMON GOTCHA:
        // After nextInt(), nextDouble() etc., nextLine() reads 
        // the leftover newline character. Add an extra nextLine():
        scanner.nextLine();  // consume leftover newline
        
        System.out.print("Enter your city: ");
        String city = scanner.nextLine();  // Now this works correctly
        System.out.println("City: " + city);
        
        // Always close the scanner when done
        scanner.close();
    }
}
```

---

## Chapter 8: Control Flow - Conditional Statements

### Theory:
Conditional statements let your program make decisions. They evaluate conditions (true/false) and execute different code blocks accordingly. In automation testing, you'll use these extensively - for example, "if element is visible, click it, else wait."

```java
public class ConditionalStatements {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // 1. IF STATEMENT
        // Executes code only if condition is true
        // ═══════════════════════════════════════
        
        int testsPassed = 45;
        int totalTests = 50;
        double passPercentage = (testsPassed * 100.0) / totalTests;
        
        if (passPercentage >= 90) {
            System.out.println("✅ Excellent! Pass rate: " + passPercentage + "%");
        }
        
        
        // ═══════════════════════════════════════
        // 2. IF-ELSE STATEMENT
        // Two paths: one for true, one for false
        // ═══════════════════════════════════════
        
        int statusCode = 404;
        
        if (statusCode == 200) {
            System.out.println("✅ Request successful");
        } else {
            System.out.println("❌ Request failed with status: " + statusCode);
        }
        
        
        // ═══════════════════════════════════════
        // 3. IF-ELSE IF-ELSE (Multiple conditions)
        // Checks conditions from top to bottom
        // Stops at the FIRST true condition
        // ═══════════════════════════════════════
        
        int httpStatus = 503;
        
        if (httpStatus >= 200 && httpStatus < 300) {
            System.out.println("✅ Success");
        } else if (httpStatus >= 300 && httpStatus < 400) {
            System.out.println("↪️ Redirection");
        } else if (httpStatus >= 400 && httpStatus < 500) {
            System.out.println("❌ Client Error");
        } else if (httpStatus >= 500) {
            System.out.println("🔥 Server Error");
        } else {
            System.out.println("❓ Unknown status");
        }
        
        // Automation Testing Example:
        String actualTitle = "Google";
        String expectedTitle = "Google";
        
        if (actualTitle.equals(expectedTitle)) {
            System.out.println("✅ TEST PASSED: Title matches");
        } else {
            System.out.println("❌ TEST FAILED: Expected '" + expectedTitle 
                             + "' but got '" + actualTitle + "'");
        }
        
        
        // ═══════════════════════════════════════
        // 4. NESTED IF (If inside If)
        // ═══════════════════════════════════════
        
        boolean isLoggedIn = true;
        String userRole = "admin";
        
        if (isLoggedIn) {
            System.out.println("User is logged in");
            
            if (userRole.equals("admin")) {
                System.out.println("Showing admin dashboard");
            } else if (userRole.equals("user")) {
                System.out.println("Showing user dashboard");
            } else {
                System.out.println("Showing guest dashboard");
            }
        } else {
            System.out.println("Please log in first");
        }
        
        
        // ═══════════════════════════════════════
        // 5. SWITCH STATEMENT
        // Better than multiple if-else when checking 
        // one variable against many values
        // ═══════════════════════════════════════
        
        String browser = "chrome";
        
        switch (browser.toLowerCase()) {
            case "chrome":
                System.out.println("Launching Chrome browser");
                // WebDriver driver = new ChromeDriver();
                break;  // ⚠️ IMPORTANT: without break, execution falls through!
                
            case "firefox":
                System.out.println("Launching Firefox browser");
                // WebDriver driver = new FirefoxDriver();
                break;
                
            case "edge":
                System.out.println("Launching Edge browser");
                // WebDriver driver = new EdgeDriver();
                break;
                
            case "safari":
                System.out.println("Launching Safari browser");
                break;
                
            default:  // Like 'else' - runs when no case matches
                System.out.println("❌ Unsupported browser: " + browser);
                break;
        }
        
        // Enhanced Switch (Java 14+) - Cleaner syntax
        String day = "MONDAY";
        String dayType = switch (day) {
            case "MONDAY", "TUESDAY", "WEDNESDAY", "THURSDAY", "FRIDAY" -> "Weekday";
            case "SATURDAY", "SUNDAY" -> "Weekend";
            default -> "Invalid day";
        };
        System.out.println(day + " is a " + dayType);
    }
}
```

---

## Chapter 9: Control Flow - Loops

### Theory:
Loops allow you to repeat a block of code multiple times. In automation testing, loops are essential for:
- Iterating through test data
- Retrying failed operations
- Processing multiple web elements
- Running the same test with different inputs

```java
public class Loops {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // 1. FOR LOOP
        // Use when: you KNOW how many times to repeat
        // Syntax: for(initialization; condition; update)
        // ═══════════════════════════════════════
        
        System.out.println("=== FOR LOOP ===");
        
        // Basic for loop
        for (int i = 1; i <= 5; i++) {
            System.out.println("Test Case " + i + ": Running...");
        }
        
        // How it works step by step:
        // Step 1: i = 1 (initialization - runs ONCE)
        // Step 2: Is 1 <= 5? YES → execute body → i++ → i = 2
        // Step 3: Is 2 <= 5? YES → execute body → i++ → i = 3
        // Step 4: Is 3 <= 5? YES → execute body → i++ → i = 4
        // Step 5: Is 4 <= 5? YES → execute body → i++ → i = 5
        // Step 6: Is 5 <= 5? YES → execute body → i++ → i = 6
        // Step 7: Is 6 <= 5? NO → EXIT loop
        
        // Counting backwards
        System.out.println("\nCountdown:");
        for (int i = 10; i >= 1; i--) {
            System.out.println(i);
        }
        System.out.println("🚀 Launch!");
        
        // Loop with step/increment of 2
        System.out.println("\nEven numbers 1-20:");
        for (int i = 2; i <= 20; i += 2) {
            System.out.print(i + " ");
        }
        System.out.println();
        
        
        // ═══════════════════════════════════════
        // 2. WHILE LOOP
        // Use when: you DON'T know how many times 
        // to repeat, but know the condition to stop
        // Checks condition BEFORE executing
        // ═══════════════════════════════════════
        
        System.out.println("\n=== WHILE LOOP ===");
        
        // Simulating retry logic (very common in testing!)
        int maxRetries = 3;
        int attempt = 1;
        boolean isElementFound = false;
        
        while (attempt <= maxRetries && !isElementFound) {
            System.out.println("Attempt " + attempt + ": Looking for element...");
            
            // Simulate: element found on 3rd attempt
            if (attempt == 3) {
                isElementFound = true;
                System.out.println("✅ Element found!");
            } else {
                System.out.println("❌ Element not found. Retrying...");
            }
            attempt++;
        }
        
        if (!isElementFound) {
            System.out.println("🔥 Element not found after " + maxRetries + " attempts");
        }
        
        
        // ═══════════════════════════════════════
        // 3. DO-WHILE LOOP
        // Use when: you want to execute AT LEAST ONCE
        // Checks condition AFTER executing
        // ═══════════════════════════════════════
        
        System.out.println("\n=== DO-WHILE LOOP ===");
        
        int menuChoice;
        Scanner scanner = new Scanner(System.in);
        
        // This will always execute at least once
        // do {
        //     System.out.println("1. Run Tests");
        //     System.out.println("2. View Report");
        //     System.out.println("3. Exit");
        //     System.out.print("Enter choice: ");
        //     menuChoice = scanner.nextInt();
        // } while (menuChoice != 3);
        
        // Simple example:
        int number = 1;
        do {
            System.out.println("Number: " + number);
            number++;
        } while (number <= 5);
        
        
        // ═══════════════════════════════════════
        // 4. FOR-EACH LOOP (Enhanced For Loop)
        // Use when: iterating through arrays/collections
        // Cleaner syntax, no index management
        // ═══════════════════════════════════════
        
        System.out.println("\n=== FOR-EACH LOOP ===");
        
        String[] browsers = {"Chrome", "Firefox", "Edge", "Safari"};
        
        for (String browser : browsers) {
            System.out.println("Testing on: " + browser);
        }
        
        
        // ═══════════════════════════════════════
        // 5. BREAK AND CONTINUE
        // ═══════════════════════════════════════
        
        System.out.println("\n=== BREAK ===");
        // BREAK: Exit the loop immediately
        for (int i = 1; i <= 10; i++) {
            if (i == 5) {
                System.out.println("Critical error at test " + i + "! Stopping.");
                break;  // Exit the loop
            }
            System.out.println("Test " + i + ": Passed");
        }
        
        System.out.println("\n=== CONTINUE ===");
        // CONTINUE: Skip current iteration, go to next
        for (int i = 1; i <= 10; i++) {
            if (i == 3 || i == 7) {
                System.out.println("Test " + i + ": Skipped (known issue)");
                continue;  // Skip to next iteration
            }
            System.out.println("Test " + i + ": Executed");
        }
        
        
        // ═══════════════════════════════════════
        // 6. NESTED LOOPS
        // ═══════════════════════════════════════
        
        System.out.println("\n=== NESTED LOOPS ===");
        
        String[] environments = {"Dev", "QA", "Staging"};
        String[] testSuites = {"Smoke", "Regression"};
        
        for (String env : environments) {
            for (String suite : testSuites) {
                System.out.println("Running " + suite + " tests on " + env);
            }
            System.out.println("---");
        }
    }
}
```

### Loop Comparison Summary:
```
╔═══════════════╦══════════════════════════════════════╗
║ Loop Type     ║ When to Use                          ║
╠═══════════════╬══════════════════════════════════════╣
║ for           ║ Known number of iterations           ║
║ while         ║ Unknown iterations, check first      ║
║ do-while      ║ Execute at least once, check after   ║
║ for-each      ║ Iterating through collections        ║
╚═══════════════╩══════════════════════════════════════╝
```

---

## Chapter 10: Arrays

### Theory:
An **array** is a container that holds a **fixed number of values** of the **same data type**. Think of it as a row of numbered boxes (indexed from 0). Arrays are fundamental in testing for storing test data, element lists, and results.

```java
public class Arrays {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // 1. DECLARING AND INITIALIZING ARRAYS
        // ═══════════════════════════════════════
        
        // Method 1: Declare size, add values later
        int[] testScores = new int[5];  // Creates array of 5 integers (all 0)
        testScores[0] = 95;  // First element (index 0)
        testScores[1] = 87;
        testScores[2] = 92;
        testScores[3] = 78;
        testScores[4] = 88;
        // testScores[5] = 100;  // ❌ ArrayIndexOutOfBoundsException!
        
        // Method 2: Declare and initialize in one line
        String[] browsers = {"Chrome", "Firefox", "Edge", "Safari"};
        
        // Method 3: Using new keyword with values
        double[] prices = new double[]{19.99, 29.99, 39.99};
        
        
        // ═══════════════════════════════════════
        // 2. ACCESSING ELEMENTS
        // ═══════════════════════════════════════
        
        System.out.println("First browser: " + browsers[0]);    // Chrome
        System.out.println("Last browser: " + browsers[browsers.length - 1]);  // Safari
        System.out.println("Array length: " + browsers.length);  // 4
        
        // Visualizing array indices:
        // Index:    [0]        [1]        [2]       [3]
        // Value:  "Chrome"  "Firefox"   "Edge"   "Safari"
        
        
        // ═══════════════════════════════════════
        // 3. ITERATING THROUGH ARRAYS
        // ═══════════════════════════════════════
        
        System.out.println("\n--- Using for loop ---");
        for (int i = 0; i < browsers.length; i++) {
            System.out.println("Index " + i + ": " + browsers[i]);
        }
        
        System.out.println("\n--- Using for-each loop ---");
        for (String browser : browsers) {
            System.out.println("Testing on: " + browser);
        }
        
        
        // ═══════════════════════════════════════
        // 4. COMMON ARRAY OPERATIONS
        // ═══════════════════════════════════════
        
        int[] numbers = {64, 25, 12, 22, 11, 90, 45};
        
        // Find maximum
        int max = numbers[0];
        for (int num : numbers) {
            if (num > max) {
                max = num;
            }
        }
        System.out.println("\nMax value: " + max);
        
        // Calculate average
        int sum = 0;
        for (int num : numbers) {
            sum += num;
        }
        double average = (double) sum / numbers.length;
        System.out.println("Average: " + average);
        
        // Sort array
        java.util.Arrays.sort(numbers);
        System.out.println("Sorted: " + java.util.Arrays.toString(numbers));
        
        // Search in array
        int index = java.util.Arrays.binarySearch(numbers, 22);
        System.out.println("22 found at index: " + index);
        
        // Copy array
        int[] copyOfNumbers = java.util.Arrays.copyOf(numbers, numbers.length);
        
        // Compare arrays
        boolean areEqual = java.util.Arrays.equals(numbers, copyOfNumbers);
        System.out.println("Arrays are equal: " + areEqual);
        
        
        // ═══════════════════════════════════════
        // 5. MULTI-DIMENSIONAL ARRAYS (2D Arrays)
        // Think of it as a table with rows and columns
        // ═══════════════════════════════════════
        
        System.out.println("\n=== 2D Array (Test Data Table) ===");
        
        // Test data: [username, password, expected result]
        String[][] testData = {
            {"admin", "admin123", "Success"},
            {"user", "user123", "Success"},
            {"admin", "wrong", "Failure"},
            {"", "", "Failure"},
            {"admin", "", "Failure"}
        };
        
        // Print header
        System.out.printf("%-12s %-12s %-12s%n", "Username", "Password", "Expected");
        System.out.println("------------------------------------");
        
        // Iterate through 2D array
        for (int i = 0; i < testData.length; i++) {
            String username = testData[i][0];
            String password = testData[i][1];
            String expected = testData[i][2];
            
            System.out.printf("%-12s %-12s %-12s%n", 
                username.isEmpty() ? "(empty)" : username, 
                password.isEmpty() ? "(empty)" : password, 
                expected);
        }
        
        
        // ═══════════════════════════════════════
        // 6. JAGGED ARRAYS (Arrays of different lengths)
        // ═══════════════════════════════════════
        
        int[][] jaggedArray = new int[3][];
        jaggedArray[0] = new int[]{1, 2, 3};
        jaggedArray[1] = new int[]{4, 5};
        jaggedArray[2] = new int[]{6, 7, 8, 9};
        
        for (int[] row : jaggedArray) {
            for (int val : row) {
                System.out.print(val + " ");
            }
            System.out.println();
        }
    }
}
```

---

## Chapter 11: Strings in Detail

### Theory:
Strings are one of the most used data types in automation testing. You'll constantly work with text - URLs, element text, error messages, test data, etc. In Java, Strings are **immutable** (cannot be changed after creation). Every modification creates a new String object.

```java
public class StringOperations {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // 1. CREATING STRINGS
        // ═══════════════════════════════════════
        
        String s1 = "Hello";            // String literal (uses String Pool)
        String s2 = "Hello";            // Points to same object in pool
        String s3 = new String("Hello"); // New object in heap (different reference)
        
        // String Pool Visualization:
        // ┌─────────────────────────────────┐
        // │         HEAP MEMORY             │
        // │  ┌──────────────────┐           │
        // │  │   STRING POOL    │           │
        // │  │   ┌─────────┐   │           │
        // │  │   │ "Hello" │ ← s1, s2      │
        // │  │   └─────────┘   │           │
        // │  └──────────────────┘           │
        // │                                 │
        // │  ┌─────────┐                    │
        // │  │ "Hello" │ ← s3 (separate!)  │
        // │  └─────────┘                    │
        // └─────────────────────────────────┘
        
        System.out.println(s1 == s2);       // true (same reference)
        System.out.println(s1 == s3);       // false (different references!)
        System.out.println(s1.equals(s3));  // true (same content)
        // ⚠️ RULE: ALWAYS use .equals() to compare strings, not ==
        
        
        // ═══════════════════════════════════════
        // 2. ESSENTIAL STRING METHODS
        // (You'll use these DAILY in testing!)
        // ═══════════════════════════════════════
        
        String url = "  https://www.Google.com/search?q=selenium  ";
        String errorMsg = "Error: Element not found on page";
        String email = "john.doe@gmail.com";
        
        // --- Length ---
        System.out.println("Length: " + url.length());  // includes spaces!
        
        // --- Trim (Remove leading/trailing whitespace) ---
        String trimmedUrl = url.trim();
        System.out.println("Trimmed: '" + trimmedUrl + "'");
        
        // --- Case Conversion ---
        System.out.println("Upper: " + trimmedUrl.toUpperCase());
        System.out.println("Lower: " + trimmedUrl.toLowerCase());
        
        // --- Checking Content ---
        System.out.println("Contains 'Google': " + trimmedUrl.contains("Google"));   // true
        System.out.println("Contains 'google': " + trimmedUrl.contains("google"));   // false (case-sensitive!)
        System.out.println("Starts with 'https': " + trimmedUrl.startsWith("https")); // true
        System.out.println("Ends with '.com': " + email.endsWith(".com"));   // true
        System.out.println("Is empty: " + url.isEmpty());        // false
        System.out.println("Is blank: " + "   ".isBlank());      // true (Java 11+)
        
        // --- Finding Position ---
        System.out.println("Index of '@': " + email.indexOf('@'));     // 8
        System.out.println("Last index of '.': " + email.lastIndexOf('.')); // 13
        
        // --- Extracting Parts (Substring) ---
        String domain = email.substring(email.indexOf('@') + 1);
        System.out.println("Domain: " + domain);  // gmail.com
        
        String protocol = trimmedUrl.substring(0, 5);
        System.out.println("Protocol: " + protocol);  // https
        
        // --- Replacing ---
        String newUrl = trimmedUrl.replace("Google", "Bing");
        System.out.println("Replaced: " + newUrl);
        
        // Replace all occurrences using regex
        String cleaned = "Test  Case   001".replaceAll("\\s+", " ");
        System.out.println("Cleaned: " + cleaned);  // "Test Case 001"
        
        // --- Splitting ---
        String csvData = "John,Doe,25,Engineer";
        String[] parts = csvData.split(",");
        for (String part : parts) {
            System.out.println("Part: " + part);
        }
        // Output: John, Doe, 25, Engineer
        
        // --- Joining ---
        String joined = String.join(" | ", parts);
        System.out.println("Joined: " + joined);  // John | Doe | 25 | Engineer
        
        // --- Character Extraction ---
        char firstChar = email.charAt(0);
        System.out.println("First char: " + firstChar);  // j
        
        // --- Comparing ---
        String str1 = "Apple";
        String str2 = "Banana";
        System.out.println("Compare: " + str1.compareTo(str2));  // negative (Apple < Banana)
        System.out.println("Equals ignore case: " + 
            "HELLO".equalsIgnoreCase("hello"));  // true
        
        
        // ═══════════════════════════════════════
        // 3. STRING CONCATENATION
        // ═══════════════════════════════════════
        
        String firstName = "John";
        String lastName = "Doe";
        
        // Method 1: + operator (creates many temp objects - slow in loops)
        String fullName1 = firstName + " " + lastName;
        
        // Method 2: concat() method
        String fullName2 = firstName.concat(" ").concat(lastName);
        
        // Method 3: String.format() (like printf)
        String fullName3 = String.format("%s %s", firstName, lastName);
        
        // Method 4: StringBuilder (BEST for multiple concatenations)
        StringBuilder sb = new StringBuilder();
        sb.append(firstName);
        sb.append(" ");
        sb.append(lastName);
        String fullName4 = sb.toString();
        
        System.out.println("Full name: " + fullName4);
        
        
        // ═══════════════════════════════════════
        // 4. STRINGBUILDER (Mutable strings)
        // Use when building strings in loops
        // ═══════════════════════════════════════
        
        StringBuilder report = new StringBuilder();
        report.append("Test Execution Report\n");
        report.append("=====================\n");
        
        String[] testCases = {"Login Test", "Search Test", "Checkout Test"};
        String[] results = {"PASS", "FAIL", "PASS"};
        
        for (int i = 0; i < testCases.length; i++) {
            report.append(String.format("%-20s: %s%n", testCases[i], results[i]));
        }
        
        report.append("=====================\n");
        report.append("Total: ").append(testCases.length).append(" tests");
        
        System.out.println(report.toString());
        
        
        // ═══════════════════════════════════════
        // 5. PRACTICAL TESTING EXAMPLES
        // ═══════════════════════════════════════
        
        // Validate email format (basic)
        String testEmail = "user@example.com";
        boolean isValidEmail = testEmail.contains("@") 
                            && testEmail.contains(".") 
                            && testEmail.indexOf("@") < testEmail.lastIndexOf(".");
        System.out.println("Valid email: " + isValidEmail);
        
        // Extract file extension
        String fileName = "test_report.html";
        String extension = fileName.substring(fileName.lastIndexOf('.') + 1);
        System.out.println("Extension: " + extension);  // html
        
        // Build dynamic XPath (common in Selenium)
        String linkText = "Login";
        String xpath = String.format("//a[text()='%s']", linkText);
        System.out.println("XPath: " + xpath);
        // Output: //a[text()='Login']
    }
}
```

---

## 📝 PHASE 1 PRACTICE EXERCISES

```java
/*
 * Exercise 1: Create a program that:
 * - Takes a student's name and 5 test scores
 * - Calculates the average
 * - Assigns a grade (A: 90+, B: 80-89, C: 70-79, D: 60-69, F: below 60)
 * - Prints a formatted report card
 *
 * Exercise 2: Create a multiplication table (1-12) using nested loops
 *
 * Exercise 3: Write a program that:
 * - Takes a sentence as input
 * - Counts vowels, consonants, digits, and spaces
 * - Reverses the sentence
 * - Checks if it's a palindrome
 *
 * Exercise 4: Create a test data array with 5 login credentials
 * - Iterate through each and simulate login validation
 * - Print PASS/FAIL for each
 * - Print total passed/failed count at the end
 */
```

---

---
