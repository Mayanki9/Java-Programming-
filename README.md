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

# 📗 PHASE 2: OBJECT-ORIENTED PROGRAMMING (Weeks 5-8)

---

## Chapter 12: Introduction to OOP

### Theory:
Object-Oriented Programming (OOP) is a programming paradigm based on the concept of "objects" which contain **data (fields/attributes)** and **code (methods/behaviors)**. It's the backbone of Java and essential for automation frameworks like the Page Object Model.

### The 4 Pillars of OOP:
```
┌──────────────────────────────────────────────┐
│           4 PILLARS OF OOP                    │
├──────────────┬───────────────────────────────┤
│ Encapsulation│ Bundling data + methods       │
│              │ Hiding internal details       │
├──────────────┼───────────────────────────────┤
│ Inheritance  │ Child class inherits from     │
│              │ parent class                  │
├──────────────┼───────────────────────────────┤
│ Polymorphism │ Same method, different        │
│              │ behaviors                     │
├──────────────┼───────────────────────────────┤
│ Abstraction  │ Show only essential features  │
│              │ Hide complexity               │
└──────────────┴───────────────────────────────┘
```

### Real World Analogy:
```
CLASS = Blueprint of a Car
OBJECT = An actual car built from that blueprint

CLASS "Car":
  - Data/Attributes: color, brand, speed, fuel
  - Methods/Behaviors: start(), accelerate(), brake(), stop()

OBJECT 1: Red Toyota, 60mph, Full tank
OBJECT 2: Blue Honda, 0mph, Half tank
```

---

## Chapter 13: Classes and Objects

```java
// ═══════════════════════════════════════
// FILE: Car.java - Defining a Class
// ═══════════════════════════════════════

public class Car {
    
    // ATTRIBUTES (Fields/Properties/Instance Variables)
    // These describe the characteristics of the object
    String brand;
    String color;
    int year;
    double speed;
    boolean isRunning;
    
    // CONSTRUCTOR: Special method called when creating an object
    // Same name as class, no return type
    
    // Default constructor (no parameters)
    public Car() {
        this.brand = "Unknown";
        this.color = "White";
        this.year = 2024;
        this.speed = 0;
        this.isRunning = false;
        System.out.println("A car has been created with default values!");
    }
    
    // Parameterized constructor
    public Car(String brand, String color, int year) {
        this.brand = brand;      // 'this' refers to the current object
        this.color = color;      // distinguishes field from parameter
        this.year = year;
        this.speed = 0;
        this.isRunning = false;
        System.out.println("A " + color + " " + brand + " has been created!");
    }
    
    // METHODS (Behaviors/Functions)
    
    public void start() {
        if (!isRunning) {
            isRunning = true;
            System.out.println(brand + " started! 🚗");
        } else {
            System.out.println(brand + " is already running!");
        }
    }
    
    public void accelerate(double amount) {
        if (isRunning) {
            speed += amount;
            System.out.println(brand + " accelerating. Speed: " + speed + " mph");
        } else {
            System.out.println("Start the car first!");
        }
    }
    
    public void brake() {
        if (speed > 0) {
            speed -= 10;
            if (speed < 0) speed = 0;
            System.out.println(brand + " braking. Speed: " + speed + " mph");
        }
    }
    
    public void stop() {
        isRunning = false;
        speed = 0;
        System.out.println(brand + " stopped! 🅿️");
    }
    
    // Method that returns a value
    public String getDetails() {
        return String.format("%d %s %s - Speed: %.1f mph - %s",
            year, color, brand, speed, isRunning ? "Running" : "Stopped");
    }
}

// ═══════════════════════════════════════
// FILE: CarDemo.java - Using the Class
// ═══════════════════════════════════════

public class CarDemo {
    public static void main(String[] args) {
        
        // Creating objects (instances) of Car class
        Car car1 = new Car("Toyota", "Red", 2023);
        Car car2 = new Car("Honda", "Blue", 2024);
        Car car3 = new Car();  // Uses default constructor
        
        // Using methods on objects
        car1.start();
        car1.accelerate(30);
        car1.accelerate(20);
        car1.brake();
        
        System.out.println("\n" + car1.getDetails());
        System.out.println(car2.getDetails());
        System.out.println(car3.getDetails());
        
        // Modifying attributes directly (we'll learn to prevent this later)
        car3.brand = "BMW";
        car3.color = "Black";
        System.out.println("\n" + car3.getDetails());
    }
}
```

### Automation Testing Example - Page Object:
```java
// This is a preview of how OOP is used in testing
// You'll fully understand this in Phase 5

public class LoginPage {
    // Attributes (web elements)
    String usernameFieldId = "username";
    String passwordFieldId = "password";
    String loginButtonId = "loginBtn";
    String errorMessageId = "error";
    
    // Methods (page actions)
    public void enterUsername(String username) {
        System.out.println("Entering username: " + username);
        // driver.findElement(By.id(usernameFieldId)).sendKeys(username);
    }
    
    public void enterPassword(String password) {
        System.out.println("Entering password: ****");
        // driver.findElement(By.id(passwordFieldId)).sendKeys(password);
    }
    
    public void clickLogin() {
        System.out.println("Clicking login button");
        // driver.findElement(By.id(loginButtonId)).click();
    }
    
    public void login(String username, String password) {
        enterUsername(username);
        enterPassword(password);
        clickLogin();
    }
}
```

---

## Chapter 14: Methods in Detail

### Theory:
Methods are blocks of code that perform a specific task. They promote **code reusability** (write once, use many times) and **modularity** (break complex logic into smaller pieces).

```java
public class MethodsInDetail {
    
    // ═══════════════════════════════════════
    // 1. METHOD ANATOMY
    // ═══════════════════════════════════════
    
    // [access modifier] [return type] [methodName]([parameters]) {
    //     // method body
    //     return value; // if return type is not void
    // }
    
    // Method with no parameters, no return value
    public static void greet() {
        System.out.println("Hello! Welcome to Testing!");
    }
    
    // Method with parameters
    public static void greetUser(String name) {
        System.out.println("Hello, " + name + "! Welcome!");
    }
    
    // Method with return value
    public static int add(int a, int b) {
        return a + b;  // Returns the result back to the caller
    }
    
    // Method with multiple parameters and return
    public static double calculateAverage(int[] scores) {
        int sum = 0;
        for (int score : scores) {
            sum += score;
        }
        return (double) sum / scores.length;
    }
    
    // Method returning boolean (very common in testing!)
    public static boolean isValidEmail(String email) {
        return email != null 
            && email.contains("@") 
            && email.contains(".") 
            && email.indexOf("@") > 0
            && email.indexOf("@") < email.lastIndexOf(".");
    }
    
    // ═══════════════════════════════════════
    // 2. METHOD OVERLOADING
    // Same method name, different parameters
    // Java knows which to call based on arguments
    // ═══════════════════════════════════════
    
    public static int multiply(int a, int b) {
        System.out.println("Called: multiply(int, int)");
        return a * b;
    }
    
    public static double multiply(double a, double b) {
        System.out.println("Called: multiply(double, double)");
        return a * b;
    }
    
    public static int multiply(int a, int b, int c) {
        System.out.println("Called: multiply(int, int, int)");
        return a * b * c;
    }
    
    // ═══════════════════════════════════════
    // 3. VARARGS (Variable Arguments)
    // Accepts any number of arguments
    // ═══════════════════════════════════════
    
    public static int sum(int... numbers) {  // '...' means any number of ints
        int total = 0;
        for (int num : numbers) {
            total += num;
        }
        return total;
    }
    
    // ═══════════════════════════════════════
    // 4. STATIC vs INSTANCE METHODS
    // ═══════════════════════════════════════
    
    // Static method: belongs to CLASS, called without creating object
    public static String getAppName() {
        return "Test Automation Framework";
    }
    
    // Instance method: belongs to OBJECT, needs an object to call
    public String getInstanceInfo() {
        return "This is an instance method";
    }
    
    // ═══════════════════════════════════════
    // MAIN METHOD - Testing everything
    // ═══════════════════════════════════════
    
    public static void main(String[] args) {
        // Calling methods
        greet();
        greetUser("John");
        
        int result = add(5, 3);
        System.out.println("5 + 3 = " + result);
        
        int[] scores = {85, 92, 78, 95, 88};
        System.out.println("Average: " + calculateAverage(scores));
        
        // Email validation
        System.out.println("Valid email? " + isValidEmail("john@gmail.com"));  // true
        System.out.println("Valid email? " + isValidEmail("johngmail.com"));   // false
        
        // Method overloading
        System.out.println(multiply(5, 3));        // calls int version
        System.out.println(multiply(5.5, 3.2));    // calls double version
        System.out.println(multiply(2, 3, 4));     // calls three-param version
        
        // Varargs
        System.out.println("Sum: " + sum(1, 2, 3));           // 6
        System.out.println("Sum: " + sum(1, 2, 3, 4, 5));     // 15
        System.out.println("Sum: " + sum(10));                 // 10
        
        // Static vs Instance
        System.out.println(getAppName());  // Static - no object needed
        
        MethodsInDetail obj = new MethodsInDetail();
        System.out.println(obj.getInstanceInfo());  // Instance - needs object
    }
}
```

---

## Chapter 15: Encapsulation

### Theory:
Encapsulation means **wrapping data (variables) and methods together** as a single unit, and **restricting direct access** to the internal data. We use **private** fields and **public getter/setter** methods. This is like a TV remote - you press buttons (methods) without knowing the internal circuitry (data).

### Why Encapsulation?
1. **Data Protection:** Prevents invalid data from being set
2. **Flexibility:** Can change internal implementation without affecting external code
3. **Control:** Add validation logic in setters

```java
// ═══════════════════════════════════════
// Encapsulated Class
// ═══════════════════════════════════════

public class BankAccount {
    
    // Private fields - can't be accessed directly from outside
    private String accountHolder;
    private String accountNumber;
    private double balance;
    private String pin;
    
    // Constructor
    public BankAccount(String accountHolder, String accountNumber, String pin) {
        this.accountHolder = accountHolder;
        this.accountNumber = accountNumber;
        this.pin = pin;
        this.balance = 0.0;
    }
    
    // ═══════════════════════════════════════
    // GETTERS - Read access (accessor methods)
    // ═══════════════════════════════════════
    
    public String getAccountHolder() {
        return accountHolder;
    }
    
    public String getAccountNumber() {
        // Return masked account number for security
        return "****" + accountNumber.substring(accountNumber.length() - 4);
    }
    
    public double getBalance() {
        return balance;
    }
    
    // No getter for PIN - it should never be exposed!
    
    // ═══════════════════════════════════════
    // SETTERS - Write access (mutator methods)
    // With validation!
    // ═══════════════════════════════════════
    
    public void setAccountHolder(String accountHolder) {
        if (accountHolder != null && !accountHolder.trim().isEmpty()) {
            this.accountHolder = accountHolder;
        } else {
            System.out.println("❌ Invalid name!");
        }
    }
    
    // No setter for accountNumber - shouldn't be changed!
    // No setter for balance - use deposit/withdraw instead!
    
    public boolean setPin(String oldPin, String newPin) {
        if (oldPin.equals(this.pin)) {
            if (newPin.length() == 4 && newPin.matches("\\d+")) {
                this.pin = newPin;
                System.out.println("✅ PIN updated successfully");
                return true;
            } else {
                System.out.println("❌ PIN must be exactly 4 digits");
            }
        } else {
            System.out.println("❌ Incorrect old PIN");
        }
        return false;
    }
    
    // ═══════════════════════════════════════
    // BUSINESS METHODS - Controlled access to data
    // ═══════════════════════════════════════
    
    public boolean deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("✅ Deposited: $" + amount);
            System.out.println("   New balance: $" + balance);
            return true;
        } else {
            System.out.println("❌ Deposit amount must be positive!");
            return false;
        }
    }
    
    public boolean withdraw(double amount, String pin) {
        if (!pin.equals(this.pin)) {
            System.out.println("❌ Incorrect PIN!");
            return false;
        }
        if (amount <= 0) {
            System.out.println("❌ Withdrawal amount must be positive!");
            return false;
        }
        if (amount > balance) {
            System.out.println("❌ Insufficient funds! Balance: $" + balance);
            return false;
        }
        
        balance -= amount;
        System.out.println("✅ Withdrawn: $" + amount);
        System.out.println("   Remaining balance: $" + balance);
        return true;
    }
    
    @Override
    public String toString() {
        return String.format("Account: %s | Holder: %s | Balance: $%.2f",
            getAccountNumber(), accountHolder, balance);
    }
}

// ═══════════════════════════════════════
// Using the Encapsulated Class
// ═══════════════════════════════════════

public class BankDemo {
    public static void main(String[] args) {
        BankAccount account = new BankAccount("John Doe", "1234567890", "1234");
        
        // ❌ Can't access private fields directly:
        // account.balance = 1000000;  // Compilation error!
        // account.pin = "0000";       // Compilation error!
        
        // ✅ Must use public methods:
        account.deposit(1000);
        account.deposit(500);
        account.withdraw(200, "1234");
        account.withdraw(200, "wrong");  // Wrong PIN
        account.withdraw(5000, "1234");  // Insufficient funds
        
        System.out.println("\n" + account.toString());
        System.out.println("Account number: " + account.getAccountNumber()); // Masked!
    }
}
```

### Testing-Relevant Encapsulation Example:
```java
public class TestConfiguration {
    private String browser;
    private String baseUrl;
    private int implicitWait;
    private boolean headless;
    
    public TestConfiguration() {
        // Default values
        this.browser = "chrome";
        this.baseUrl = "https://www.example.com";
        this.implicitWait = 10;
        this.headless = false;
    }
    
    public String getBrowser() { return browser; }
    
    public void setBrowser(String browser) {
        String[] validBrowsers = {"chrome", "firefox", "edge", "safari"};
        for (String valid : validBrowsers) {
            if (valid.equalsIgnoreCase(browser)) {
                this.browser = browser.toLowerCase();
                return;
            }
        }
        throw new IllegalArgumentException("Unsupported browser: " + browser);
    }
    
    public void setImplicitWait(int seconds) {
        if (seconds >= 0 && seconds <= 60) {
            this.implicitWait = seconds;
        } else {
            throw new IllegalArgumentException("Wait must be 0-60 seconds");
        }
    }
    
    // ... other getters and setters
}
```

---

## Chapter 16: Inheritance

### Theory:
Inheritance is the mechanism where a new class (**child/subclass**) acquires the properties and behaviors of an existing class (**parent/superclass**). It promotes **code reuse** and establishes a natural **"IS-A" relationship**.

```
ANALOGY:
    Animal (Parent)
      ├── Dog (Child) - IS-A Animal
      ├── Cat (Child) - IS-A Animal
      └── Bird (Child) - IS-A Animal
      
    All animals can eat() and sleep()
    But each has its own makeSound()
```

```java
// ═══════════════════════════════════════
// PARENT CLASS (Superclass/Base class)
// ═══════════════════════════════════════

public class Animal {
    // Protected: accessible in same package AND subclasses
    protected String name;
    protected int age;
    protected String color;
    
    public Animal(String name, int age, String color) {
        this.name = name;
        this.age = age;
        this.color = color;
        System.out.println("Animal constructor called");
    }
    
    public void eat() {
        System.out.println(name + " is eating 🍽️");
    }
    
    public void sleep() {
        System.out.println(name + " is sleeping 😴");
    }
    
    public void makeSound() {
        System.out.println(name + " makes a sound");
    }
    
    public String getInfo() {
        return String.format("%s - Age: %d, Color: %s", name, age, color);
    }
}

// ═══════════════════════════════════════
// CHILD CLASS 1 (Subclass/Derived class)
// Uses 'extends' keyword
// ═══════════════════════════════════════

public class Dog extends Animal {
    // Additional field specific to Dog
    private String breed;
    
    public Dog(String name, int age, String color, String breed) {
        super(name, age, color);  // Call parent's constructor FIRST
        this.breed = breed;
        System.out.println("Dog constructor called");
    }
    
    // METHOD OVERRIDING: Redefining parent's method
    @Override  // Annotation - tells compiler we're overriding
    public void makeSound() {
        System.out.println(name + " says: Woof! Woof! 🐕");
    }
    
    // New method specific to Dog
    public void fetch() {
        System.out.println(name + " is fetching the ball! 🎾");
    }
    
    @Override
    public String getInfo() {
        return super.getInfo() + ", Breed: " + breed;
    }
}

// ═══════════════════════════════════════
// CHILD CLASS 2
// ═══════════════════════════════════════

public class Cat extends Animal {
    private boolean isIndoor;
    
    public Cat(String name, int age, String color, boolean isIndoor) {
        super(name, age, color);
        this.isIndoor = isIndoor;
    }
    
    @Override
    public void makeSound() {
        System.out.println(name + " says: Meow! 🐱");
    }
    
    public void purr() {
        System.out.println(name + " is purring... 😸");
    }
}

// ═══════════════════════════════════════
// DEMO
// ═══════════════════════════════════════

public class InheritanceDemo {
    public static void main(String[] args) {
        Dog dog = new Dog("Buddy", 3, "Golden", "Labrador");
        Cat cat = new Cat("Whiskers", 2, "White", true);
        
        // Inherited methods
        dog.eat();        // From Animal
        dog.sleep();      // From Animal
        dog.makeSound();  // Overridden in Dog
        dog.fetch();      // Dog's own method
        
        System.out.println();
        
        cat.eat();        // From Animal
        cat.makeSound();  // Overridden in Cat
        cat.purr();       // Cat's own method
        
        System.out.println("\n" + dog.getInfo());
        System.out.println(cat.getInfo());
        
        // IS-A relationship
        System.out.println("\ndog IS-A Animal: " + (dog instanceof Animal));  // true
        System.out.println("cat IS-A Animal: " + (cat instanceof Animal));  // true
    }
}
```

### Inheritance in Automation Testing (Preview):
```java
// Base test class - common setup/teardown for all tests
public class BaseTest {
    protected String browser;
    protected String baseUrl;
    // protected WebDriver driver;
    
    public void setUp() {
        System.out.println("Opening browser: " + browser);
        System.out.println("Navigating to: " + baseUrl);
        // driver = new ChromeDriver();
        // driver.get(baseUrl);
    }
    
    public void tearDown() {
        System.out.println("Closing browser");
        // driver.quit();
    }
    
    public void takeScreenshot(String testName) {
        System.out.println("Screenshot saved for: " + testName);
    }
}

// Login tests inherit common behavior
public class LoginTest extends BaseTest {
    
    public LoginTest() {
        this.browser = "Chrome";
        this.baseUrl = "https://app.example.com/login";
    }
    
    public void testValidLogin() {
        setUp();  // Inherited from BaseTest
        System.out.println("Running: testValidLogin");
        // Test-specific code here
        tearDown();  // Inherited from BaseTest
    }
    
    public void testInvalidLogin() {
        setUp();
        System.out.println("Running: testInvalidLogin");
        takeScreenshot("testInvalidLogin");  // Inherited
        tearDown();
    }
}
```

### Access Modifiers Summary:
```
╔═══════════════╦═══════════╦══════════════╦════════════╦════════════╗
║   Modifier    ║ Same Class║ Same Package ║ Subclass   ║ Everywhere ║
╠═══════════════╬═══════════╬══════════════╬════════════╬════════════╣
║ private       ║    ✅     ║     ❌       ║    ❌      ║    ❌      ║
║ (default)     ║    ✅     ║     ✅       ║    ❌      ║    ❌      ║
║ protected     ║    ✅     ║     ✅       ║    ✅      ║    ❌      ║
║ public        ║    ✅     ║     ✅       ║    ✅      ║    ✅      ║
╚═══════════════╩═══════════╩══════════════╩════════════╩════════════╝
```

---

## Chapter 17: Polymorphism

### Theory:
Polymorphism means "many forms." It allows objects of different classes to be treated through the same interface. There are two types:
1. **Compile-time (Static):** Method Overloading (same name, different parameters)
2. **Runtime (Dynamic):** Method Overriding (child class redefines parent's method)

```java
// ═══════════════════════════════════════
// RUNTIME POLYMORPHISM
// ═══════════════════════════════════════

// Parent class
class Shape {
    public double calculateArea() {
        return 0;
    }
    
    public String getType() {
        return "Shape";
    }
}

class Circle extends Shape {
    private double radius;
    
    public Circle(double radius) {
        this.radius = radius;
    }
    
    @Override
    public double calculateArea() {
        return Math.PI * radius * radius;
    }
    
    @Override
    public String getType() {
        return "Circle";
    }
}

class Rectangle extends Shape {
    private double length, width;
    
    public Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }
    
    @Override
    public double calculateArea() {
        return length * width;
    }
    
    @Override
    public String getType() {
        return "Rectangle";
    }
}

class Triangle extends Shape {
    private double base, height;
    
    public Triangle(double base, double height) {
        this.base = base;
        this.height = height;
    }
    
    @Override
    public double calculateArea() {
        return 0.5 * base * height;
    }
    
    @Override
    public String getType() {
        return "Triangle";
    }
}

// ═══════════════════════════════════════
// POLYMORPHISM IN ACTION
// ═══════════════════════════════════════

public class PolymorphismDemo {
    
    // This method accepts ANY Shape - polymorphism!
    public static void printShapeInfo(Shape shape) {
        // The correct method is called at RUNTIME
        // based on the actual object type
        System.out.printf("%s - Area: %.2f%n", shape.getType(), shape.calculateArea());
    }
    
    public static void main(String[] args) {
        // Parent reference, child objects
        // This IS polymorphism
        Shape shape1 = new Circle(5);
        Shape shape2 = new Rectangle(4, 6);
        Shape shape3 = new Triangle(3, 8);
        
        // Same method call, different behaviors!
        printShapeInfo(shape1);  // Circle - Area: 78.54
        printShapeInfo(shape2);  // Rectangle - Area: 24.00
        printShapeInfo(shape3);  // Triangle - Area: 12.00
        
        // Array of shapes - all treated as Shape
        Shape[] shapes = {
            new Circle(10),
            new Rectangle(5, 5),
            new Triangle(6, 4),
            new Circle(3)
        };
        
        System.out.println("\nAll shapes:");
        double totalArea = 0;
        for (Shape s : shapes) {
            printShapeInfo(s);     // Polymorphic call
            totalArea += s.calculateArea();
        }
        System.out.printf("Total area: %.2f%n", totalArea);
        
        // instanceof check
        for (Shape s : shapes) {
            if (s instanceof Circle) {
                System.out.println(s.getType() + " is a Circle!");
            }
        }
    }
}
```

### Polymorphism in Testing (Preview):
```java
// All browser drivers implement the same interface
// WebDriver driver;  // Parent type reference

// Polymorphism determines which browser to use at runtime
// driver = new ChromeDriver();   // OR
// driver = new FirefoxDriver();  // OR
// driver = new EdgeDriver();

// Same method call works regardless of browser!
// driver.get("https://www.google.com");
// driver.findElement(By.id("search")).click();
// driver.quit();
```

---

## Chapter 18: Abstraction

### Theory:
Abstraction means **hiding complex implementation details** and showing only the essential features. It's implemented through:
1. **Abstract Classes:** Partially implemented (can have both abstract and concrete methods)
2. **Interfaces:** Fully abstract (only method signatures, no implementation) - before Java 8

### Analogy:
```
When you drive a car:
- You know: steering wheel turns the car, pedals control speed
- You DON'T know: how the engine combustion works, transmission details

The steering wheel is ABSTRACTION - simple interface, complex implementation hidden
```

```java
// ═══════════════════════════════════════
// 1. ABSTRACT CLASS
// - Cannot be instantiated (can't create objects)
// - Can have abstract methods (no body) and concrete methods (with body)
// - Child classes MUST implement abstract methods
// ═══════════════════════════════════════

public abstract class Vehicle {
    protected String brand;
    protected String model;
    protected int year;
    
    public Vehicle(String brand, String model, int year) {
        this.brand = brand;
        this.model = model;
        this.year = year;
    }
    
    // Abstract methods - MUST be implemented by child classes
    public abstract void start();
    public abstract void stop();
    public abstract double getFuelEfficiency();
    
    // Concrete method - inherited as-is
    public String getDetails() {
        return year + " " + brand + " " + model;
    }
    
    // Concrete method using abstract methods
    public void displayInfo() {
        System.out.println("Vehicle: " + getDetails());
        System.out.println("Fuel Efficiency: " + getFuelEfficiency() + " mpg");
    }
}

// Child must implement ALL abstract methods
public class ElectricCar extends Vehicle {
    private double batteryCapacity;
    
    public ElectricCar(String brand, String model, int year, double battery) {
        super(brand, model, year);
        this.batteryCapacity = battery;
    }
    
    @Override
    public void start() {
        System.out.println(getDetails() + " silently powers on ⚡");
    }
    
    @Override
    public void stop() {
        System.out.println(getDetails() + " powers off");
    }
    
    @Override
    public double getFuelEfficiency() {
        return batteryCapacity * 3.5;  // miles per charge
    }
}

public class GasCar extends Vehicle {
    private double tankSize;
    
    public GasCar(String brand, String model, int year, double tankSize) {
        super(brand, model, year);
        this.tankSize = tankSize;
    }
    
    @Override
    public void start() {
        System.out.println(getDetails() + " engine roars to life 🔥");
    }
    
    @Override
    public void stop() {
        System.out.println(getDetails() + " engine turns off");
    }
    
    @Override
    public double getFuelEfficiency() {
        return tankSize * 25;  // approximate miles per tank
    }
}


// ═══════════════════════════════════════
// 2. INTERFACES
// - 100% abstraction (before Java 8)
// - A class can implement MULTIPLE interfaces
// - All methods are public and abstract by default
// - All fields are public static final by default
// ═══════════════════════════════════════

public interface Drivable {
    // Abstract methods (implicitly public abstract)
    void accelerate(double speed);
    void brake();
    double getCurrentSpeed();
    
    // Constants (implicitly public static final)
    int MAX_SPEED = 200;
    
    // Default method (Java 8+) - has implementation
    default void honk() {
        System.out.println("Beep beep! 📯");
    }
    
    // Static method (Java 8+)
    static boolean isValidSpeed(double speed) {
        return speed >= 0 && speed <= MAX_SPEED;
    }
}

public interface GPSEnabled {
    void navigate(String destination);
    String getCurrentLocation();
}

public interface Bluetooth {
    void connectDevice(String deviceName);
    void disconnect();
}

// A class can implement MULTIPLE interfaces!
public class SmartCar extends Vehicle implements Drivable, GPSEnabled, Bluetooth {
    private double currentSpeed;
    
    public SmartCar(String brand, String model, int year) {
        super(brand, model, year);
        this.currentSpeed = 0;
    }
    
    // Implementing Vehicle abstract methods
    @Override
    public void start() {
        System.out.println(getDetails() + " smart-starts 🚗");
    }
    
    @Override
    public void stop() {
        currentSpeed = 0;
        System.out.println(getDetails() + " stops");
    }
    
    @Override
    public double getFuelEfficiency() {
        return 45.0;
    }
    
    // Implementing Drivable interface
    @Override
    public void accelerate(double speed) {
        if (Drivable.isValidSpeed(speed)) {
            this.currentSpeed = speed;
            System.out.println("Accelerating to " + speed + " mph");
        }
    }
    
    @Override
    public void brake() {
        currentSpeed = Math.max(0, currentSpeed - 10);
        System.out.println("Braking... Speed: " + currentSpeed);
    }
    
    @Override
    public double getCurrentSpeed() {
        return currentSpeed;
    }
    
    // Implementing GPSEnabled interface
    @Override
    public void navigate(String destination) {
        System.out.println("Navigating to: " + destination + " 🗺️");
    }
    
    @Override
    public String getCurrentLocation() {
        return "Current Location: Downtown";
    }
    
    // Implementing Bluetooth interface
    @Override
    public void connectDevice(String deviceName) {
        System.out.println("Connected to: " + deviceName + " 📱");
    }
    
    @Override
    public void disconnect() {
        System.out.println("Bluetooth disconnected");
    }
}

// ═══════════════════════════════════════
// DEMO
// ═══════════════════════════════════════

public class AbstractionDemo {
    public static void main(String[] args) {
        // Cannot instantiate abstract class:
        // Vehicle v = new Vehicle("A", "B", 2024);  // ❌ ERROR!
        
        SmartCar tesla = new SmartCar("Tesla", "Model 3", 2024);
        tesla.start();
        tesla.accelerate(60);
        tesla.navigate("Office");
        tesla.connectDevice("iPhone");
        tesla.honk();  // Default method from interface
        tesla.displayInfo();
        tesla.stop();
    }
}
```

### Abstract Class vs Interface:
```
╔════════════════════╦══════════════════════╦════════════════════════╗
║    Feature         ║  Abstract Class      ║  Interface             ║
╠════════════════════╬══════════════════════╬════════════════════════╣
║ Methods            ║ Abstract + Concrete  ║ Abstract (+ default)   ║
║ Variables           ║ Any type             ║ public static final    ║
║ Constructor        ║ Yes                  ║ No                     ║
║ Multiple inherit.  ║ No (single only)     ║ Yes (multiple)         ║
║ Access modifiers   ║ Any                  ║ public only            ║
║ Use when           ║ IS-A relationship    ║ CAN-DO capability      ║
║                    ║ Shared code          ║ Multiple inheritance   ║
╚════════════════════╩══════════════════════╩════════════════════════╝
```

---

## Chapter 19: Static Keyword, Final Keyword, and `this` / `super`

```java
public class KeywordsExplained {
    
    // ═══════════════════════════════════════
    // STATIC - Belongs to CLASS, not objects
    // Shared among ALL instances
    // ═══════════════════════════════════════
    
    static int totalInstances = 0;       // Class-level variable
    static final String COMPANY = "TestCorp";  // Constant
    
    String instanceName;  // Instance-level variable
    
    public KeywordsExplained(String name) {
        this.instanceName = name;
        totalInstances++;  // Shared counter
    }
    
    // Static method - can only access static members
    public static int getTotalInstances() {
        // System.out.println(instanceName);  // ❌ Can't access instance variable!
        return totalInstances;
    }
    
    // Static block - runs ONCE when class is loaded
    static {
        System.out.println("Static block executed! Class loaded.");
    }
    
    // ═══════════════════════════════════════
    // FINAL - Cannot be changed/overridden
    // ═══════════════════════════════════════
    
    // final variable = CONSTANT
    final int MAX_VALUE = 100;
    
    // final method = CANNOT be overridden by child
    public final void criticalMethod() {
        System.out.println("This method cannot be overridden!");
    }
    
    // final class = CANNOT be extended (e.g., String class)
    // public final class CannotBeInherited { }
    
    
    public static void main(String[] args) {
        // Static access - no object needed
        System.out.println("Company: " + COMPANY);
        System.out.println("Instances: " + getTotalInstances());
        
        KeywordsExplained obj1 = new KeywordsExplained("First");
        KeywordsExplained obj2 = new KeywordsExplained("Second");
        KeywordsExplained obj3 = new KeywordsExplained("Third");
        
        // All objects share the same static variable
        System.out.println("Total instances: " + getTotalInstances());  // 3
    }
}
```

---

## Chapter 20: Enums

### Theory:
An **Enum** (Enumeration) is a special class that represents a group of **constants** (fixed values). Use enums when you have a predefined set of values that won't change.

```java
// ═══════════════════════════════════════
// Simple Enum
// ═══════════════════════════════════════

public enum Browser {
    CHROME,
    FIREFOX,
    EDGE,
    SAFARI
}

// ═══════════════════════════════════════
// Enum with fields and methods
// ═══════════════════════════════════════

public enum Environment {
    DEV("https://dev.example.com", "Development"),
    QA("https://qa.example.com", "Quality Assurance"),
    STAGING("https://staging.example.com", "Staging"),
    PRODUCTION("https://www.example.com", "Production");
    
    private final String url;
    private final String displayName;
    
    // Enum constructor (always private)
    Environment(String url, String displayName) {
        this.url = url;
        this.displayName = displayName;
    }
    
    public String getUrl() { return url; }
    public String getDisplayName() { return displayName; }
}

public enum TestStatus {
    PASS("✅", "green"),
    FAIL("❌", "red"),
    SKIP("⏭️", "yellow"),
    ERROR("🔥", "orange");
    
    private final String icon;
    private final String color;
    
    TestStatus(String icon, String color) {
        this.icon = icon;
        this.color = color;
    }
    
    public String getIcon() { return icon; }
    public String getColor() { return color; }
}

// ═══════════════════════════════════════
// Using Enums
// ═══════════════════════════════════════

public class EnumDemo {
    public static void main(String[] args) {
        // Simple usage
        Browser browser = Browser.CHROME;
        
        switch (browser) {
            case CHROME:
                System.out.println("Launching Chrome");
                break;
            case FIREFOX:
                System.out.println("Launching Firefox");
                break;
            default:
                System.out.println("Browser: " + browser);
        }
        
        // Enum with fields
        Environment env = Environment.QA;
        System.out.println("Testing on: " + env.getDisplayName());
        System.out.println("URL: " + env.getUrl());
        
        // Iterate through all values
        System.out.println("\nAll environments:");
        for (Environment e : Environment.values()) {
            System.out.printf("  %s: %s%n", e.name(), e.getUrl());
        }
        
        // Convert String to Enum
        String envName = "PRODUCTION";
        Environment prodEnv = Environment.valueOf(envName);
        System.out.println("\nProduction URL: " + prodEnv.getUrl());
        
        // Test results
        TestStatus[] results = {TestStatus.PASS, TestStatus.FAIL, 
                                TestStatus.PASS, TestStatus.SKIP};
        for (TestStatus status : results) {
            System.out.println(status.getIcon() + " " + status.name());
        }
    }
}
```

---

---

# 📙 PHASE 3: INTERMEDIATE JAVA (Weeks 9-12)

---

## Chapter 21: Exception Handling

### Theory:
**Exceptions** are unexpected events that disrupt the normal flow of a program. Exception handling allows you to **gracefully handle errors** instead of letting your program crash. In testing, this is critical - you don't want one failed element lookup to crash your entire test suite.

### Exception Hierarchy:
```
java.lang.Object
  └── java.lang.Throwable
       ├── java.lang.Error (Serious - don't catch these)
       │    ├── OutOfMemoryError
       │    └── StackOverflowError
       └── java.lang.Exception
            ├── IOException (Checked - must handle)
            ├── SQLException (Checked)
            ├── FileNotFoundException (Checked)
            └── RuntimeException (Unchecked - optional to handle)
                 ├── NullPointerException
                 ├── ArrayIndexOutOfBoundsException
                 ├── NumberFormatException
                 ├── ArithmeticException
                 └── IllegalArgumentException
```

```java
public class ExceptionHandling {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // 1. TRY-CATCH - Basic exception handling
        // ═══════════════════════════════════════
        
        System.out.println("=== Basic Try-Catch ===");
        try {
            int result = 10 / 0;  // This throws ArithmeticException
            System.out.println("Result: " + result);  // This line never executes
        } catch (ArithmeticException e) {
            System.out.println("Error: Cannot divide by zero!");
            System.out.println("Exception message: " + e.getMessage());
        }
        System.out.println("Program continues normally after catch!\n");
        
        
        // ═══════════════════════════════════════
        // 2. MULTIPLE CATCH BLOCKS
        // Order: specific exceptions first, general last
        // ═══════════════════════════════════════
        
        System.out.println("=== Multiple Catch ===");
        try {
            String[] names = {"Alice", "Bob"};
            // String text = null;
            // System.out.println(text.length());        // NullPointerException
            System.out.println(names[5]);               // ArrayIndexOutOfBoundsException
        } catch (NullPointerException e) {
            System.out.println("Null Pointer: " + e.getMessage());
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Index out of bounds: " + e.getMessage());
        } catch (Exception e) {
            // General catch - catches any exception not caught above
            System.out.println("General error: " + e.getMessage());
        }
        
        
        // ═══════════════════════════════════════
        // 3. TRY-CATCH-FINALLY
        // Finally block ALWAYS executes (cleanup)
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Try-Catch-Finally ===");
        // Simulating resource management
        String resource = null;
        try {
            resource = "Database Connection Opened";
            System.out.println(resource);
            
            // Simulate some operation that might fail
            int value = Integer.parseInt("abc");  // NumberFormatException
            
        } catch (NumberFormatException e) {
            System.out.println("Error: Invalid number format");
        } finally {
            // This ALWAYS runs - even if there's a return statement!
            // Perfect for cleanup: closing browser, database, files
            System.out.println("Finally: Closing resources");
            resource = null;
        }
        
        
        // ═══════════════════════════════════════
        // 4. TRY-WITH-RESOURCES (Java 7+)
        // Automatically closes resources
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Try-With-Resources ===");
        // Resources implementing AutoCloseable are automatically closed
        try (java.util.Scanner scanner = new java.util.Scanner("test data")) {
            while (scanner.hasNext()) {
                System.out.println("Read: " + scanner.next());
            }
        }  // Scanner automatically closed here
        
        
        // ═══════════════════════════════════════
        // 5. MULTI-CATCH (Java 7+)
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Multi-Catch ===");
        try {
            String text = "not a number";
            int num = Integer.parseInt(text);
        } catch (NumberFormatException | IllegalArgumentException e) {
            System.out.println("Parsing error: " + e.getMessage());
        }
        
        
        // ═══════════════════════════════════════
        // 6. THROW - Manually throwing exceptions
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Throw ===");
        try {
            validateAge(-5);
        } catch (IllegalArgumentException e) {
            System.out.println("Validation error: " + e.getMessage());
        }
        
        
        // ═══════════════════════════════════════
        // 7. PRACTICAL TESTING EXAMPLE
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Testing Example ===");
        simulateTestExecution();
    }
    
    // THROWS - Declares that this method might throw an exception
    public static void validateAge(int age) throws IllegalArgumentException {
        if (age < 0) {
            throw new IllegalArgumentException("Age cannot be negative: " + age);
        }
        if (age > 150) {
            throw new IllegalArgumentException("Age seems invalid: " + age);
        }
        System.out.println("Age is valid: " + age);
    }
    
    public static void simulateTestExecution() {
        String[] testCases = {"Login Test", "Search Test", "Checkout Test"};
        int passed = 0, failed = 0;
        
        for (String testCase : testCases) {
            try {
                System.out.println("Running: " + testCase);
                
                // Simulate: Search Test fails
                if (testCase.equals("Search Test")) {
                    throw new RuntimeException("Element not found: search_box");
                }
                
                System.out.println("  ✅ PASSED");
                passed++;
                
            } catch (Exception e) {
                System.out.println("  ❌ FAILED: " + e.getMessage());
                failed++;
                // In real testing: take screenshot, log details
            }
        }
        
        System.out.println("\nResults: " + passed + " passed, " + failed + " failed");
    }
}


// ═══════════════════════════════════════
// 8. CUSTOM EXCEPTION
// ═══════════════════════════════════════

class ElementNotFoundException extends RuntimeException {
    private String locator;
    private String page;
    
    public ElementNotFoundException(String message, String locator, String page) {
        super(message);
        this.locator = locator;
        this.page = page;
    }
    
    public String getLocator() { return locator; }
    public String getPage() { return page; }
    
    @Override
    public String toString() {
        return String.format("ElementNotFoundException: %s [Locator: %s, Page: %s]",
            getMessage(), locator, page);
    }
}

// Usage:
// throw new ElementNotFoundException("Login button not found", "id=loginBtn", "LoginPage");
```

---

## Chapter 22: Collections Framework

### Theory:
The Collections Framework provides **data structures** (ways to store and organize data) that are more flexible than arrays. Unlike arrays, collections can **grow and shrink dynamically** and offer built-in methods for searching, sorting, and manipulating data.

### Collections Hierarchy:
```
                    Collection (Interface)
                    /        |           \
                   /         |            \
                List       Set          Queue
               /    \      /    \          |
          ArrayList  LinkedList  HashSet  LinkedList
                              TreeSet
                              LinkedHashSet

                    Map (Interface - separate)
                   /        |          \
              HashMap   TreeMap   LinkedHashMap
```

### 1. ArrayList:
```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.Iterator;
import java.util.List;

public class ArrayListDemo {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // ArrayList: Dynamic array
        // - Ordered (maintains insertion order)
        // - Allows duplicates
        // - Allows null values
        // - Index-based access (fast random access)
        // - Slow at inserting/deleting in middle
        // ═══════════════════════════════════════
        
        // Creating ArrayList
        // <String> is Generics - specifies the type of elements
        List<String> browsers = new ArrayList<>();
        
        // Adding elements
        browsers.add("Chrome");
        browsers.add("Firefox");
        browsers.add("Edge");
        browsers.add("Safari");
        browsers.add("Chrome");  // Duplicates allowed!
        
        System.out.println("Browsers: " + browsers);
        System.out.println("Size: " + browsers.size());
        
        // Accessing elements
        System.out.println("First: " + browsers.get(0));
        System.out.println("Last: " + browsers.get(browsers.size() - 1));
        
        // Modifying elements
        browsers.set(1, "Firefox Developer Edition");
        
        // Removing elements
        browsers.remove("Safari");          // By value
        browsers.remove(0);                 // By index
        
        // Checking elements
        System.out.println("Contains Edge: " + browsers.contains("Edge"));
        System.out.println("Index of Edge: " + browsers.indexOf("Edge"));
        System.out.println("Is empty: " + browsers.isEmpty());
        
        // ═══════════════════════════════════════
        // ITERATING THROUGH ARRAYLIST
        // ═══════════════════════════════════════
        
        System.out.println("\n--- Iteration Methods ---");
        
        List<String> testCases = new ArrayList<>();
        testCases.add("Login Test");
        testCases.add("Search Test");
        testCases.add("Checkout Test");
        testCases.add("Payment Test");
        testCases.add("Logout Test");
        
        // Method 1: For loop
        System.out.println("For loop:");
        for (int i = 0; i < testCases.size(); i++) {
            System.out.println("  " + (i + 1) + ". " + testCases.get(i));
        }
        
        // Method 2: Enhanced for loop
        System.out.println("\nFor-each:");
        for (String test : testCases) {
            System.out.println("  Running: " + test);
        }
        
        // Method 3: Iterator
        System.out.println("\nIterator:");
        Iterator<String> iterator = testCases.iterator();
        while (iterator.hasNext()) {
            String test = iterator.next();
            System.out.println("  " + test);
            // Safe removal during iteration:
            // if (test.equals("Search Test")) iterator.remove();
        }
        
        // Method 4: forEach with Lambda (Java 8+)
        System.out.println("\nLambda forEach:");
        testCases.forEach(test -> System.out.println("  " + test));
        
        // Method 5: Stream (Java 8+)
        System.out.println("\nStream:");
        testCases.stream()
                 .filter(test -> test.contains("Test"))
                 .forEach(test -> System.out.println("  " + test));
        
        // ═══════════════════════════════════════
        // SORTING
        // ═══════════════════════════════════════
        
        List<Integer> scores = new ArrayList<>(List.of(85, 92, 78, 95, 88, 76));
        System.out.println("\nOriginal: " + scores);
        
        Collections.sort(scores);           // Ascending
        System.out.println("Ascending: " + scores);
        
        Collections.sort(scores, Collections.reverseOrder());  // Descending
        System.out.println("Descending: " + scores);
        
        // ═══════════════════════════════════════
        // USEFUL OPERATIONS
        // ═══════════════════════════════════════
        
        System.out.println("Max: " + Collections.max(scores));
        System.out.println("Min: " + Collections.min(scores));
        System.out.println("Frequency of 85: " + Collections.frequency(scores, 85));
        
        // Convert array to list
        String[] arr = {"A", "B", "C"};
        List<String> listFromArray = new ArrayList<>(java.util.Arrays.asList(arr));
        
        // Convert list to array
        String[] arrFromList = testCases.toArray(new String[0]);
        
        // Sublist
        List<String> subList = testCases.subList(1, 3);  // Index 1 to 2
        System.out.println("Sublist: " + subList);
        
        // Clear all elements
        // testCases.clear();
    }
}
```

### 2. HashMap:
```java
import java.util.HashMap;
import java.util.Map;
import java.util.LinkedHashMap;
import java.util.TreeMap;

public class HashMapDemo {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // HashMap: Key-Value pairs
        // - Keys must be unique
        // - Values can be duplicate
        // - One null key allowed
        // - Unordered (no guaranteed order)
        // - Fast lookup: O(1)
        // ═══════════════════════════════════════
        
        // Creating HashMap
        Map<String, String> testData = new HashMap<>();
        
        // Adding key-value pairs
        testData.put("username", "admin");
        testData.put("password", "admin123");
        testData.put("email", "admin@test.com");
        testData.put("role", "administrator");
        
        System.out.println("Test Data: " + testData);
        
        // Accessing values
        String username = testData.get("username");
        System.out.println("Username: " + username);
        
        // Returns null if key doesn't exist
        String phone = testData.get("phone");
        System.out.println("Phone: " + phone);  // null
        
        // getOrDefault - returns default if key missing
        String phone2 = testData.getOrDefault("phone", "Not provided");
        System.out.println("Phone: " + phone2);
        
        // Checking
        System.out.println("Has 'email' key: " + testData.containsKey("email"));
        System.out.println("Has 'admin' value: " + testData.containsValue("admin"));
        System.out.println("Size: " + testData.size());
        
        // Modifying
        testData.put("password", "newPassword123");  // Update existing
        testData.putIfAbsent("phone", "123-456-7890");  // Add only if absent
        
        // Removing
        testData.remove("role");
        testData.remove("email", "admin@test.com");  // Remove only if value matches
        
        // ═══════════════════════════════════════
        // ITERATING THROUGH HASHMAP
        // ═══════════════════════════════════════
        
        System.out.println("\n--- Iteration ---");
        
        Map<String, Integer> testResults = new HashMap<>();
        testResults.put("Login Test", 1);      // 1 = Pass
        testResults.put("Search Test", 0);     // 0 = Fail
        testResults.put("Checkout Test", 1);
        testResults.put("Payment Test", 1);
        testResults.put("Logout Test", 0);
        
        // Method 1: Entry set (most common)
        for (Map.Entry<String, Integer> entry : testResults.entrySet()) {
            String status = entry.getValue() == 1 ? "✅ PASS" : "❌ FAIL";
            System.out.println(entry.getKey() + ": " + status);
        }
        
        // Method 2: Key set
        System.out.println("\nKeys only:");
        for (String key : testResults.keySet()) {
            System.out.println("  " + key);
        }
        
        // Method 3: Values only
        System.out.println("\nValues only:");
        for (Integer value : testResults.values()) {
            System.out.println("  " + value);
        }
        
        // Method 4: Lambda (Java 8+)
        System.out.println("\nLambda:");
        testResults.forEach((test, result) -> {
            System.out.println("  " + test + " → " + (result == 1 ? "PASS" : "FAIL"));
        });
        
        
        // ═══════════════════════════════════════
        // PRACTICAL TESTING EXAMPLE
        // Configuration Management
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Config Example ===");
        
        Map<String, String> config = new HashMap<>();
        config.put("browser", "chrome");
        config.put("baseUrl", "https://www.example.com");
        config.put("implicitWait", "10");
        config.put("headless", "false");
        config.put("screenshotPath", "./screenshots/");
        
        // Read config values
        String browser = config.get("browser");
        int waitTime = Integer.parseInt(config.get("implicitWait"));
        boolean isHeadless = Boolean.parseBoolean(config.get("headless"));
        
        System.out.println("Browser: " + browser);
        System.out.println("Wait: " + waitTime + "s");
        System.out.println("Headless: " + isHeadless);
        
        
        // ═══════════════════════════════════════
        // LinkedHashMap: Maintains insertion order
        // TreeMap: Sorted by keys
        // ═══════════════════════════════════════
        
        Map<String, String> linked = new LinkedHashMap<>();
        linked.put("C", "3");
        linked.put("A", "1");
        linked.put("B", "2");
        System.out.println("\nLinkedHashMap: " + linked);  // {C=3, A=1, B=2}
        
        Map<String, String> tree = new TreeMap<>();
        tree.put("C", "3");
        tree.put("A", "1");
        tree.put("B", "2");
        System.out.println("TreeMap: " + tree);  // {A=1, B=2, C=3} (sorted)
    }
}
```

### 3. HashSet:
```java
import java.util.HashSet;
import java.util.Set;
import java.util.TreeSet;

public class HashSetDemo {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // HashSet: Collection of UNIQUE elements
        // - No duplicates allowed
        // - No guaranteed order
        // - Allows one null
        // - Fast lookup: O(1)
        // ═══════════════════════════════════════
        
        Set<String> uniqueBrowsers = new HashSet<>();
        uniqueBrowsers.add("Chrome");
        uniqueBrowsers.add("Firefox");
        uniqueBrowsers.add("Chrome");   // Duplicate - ignored!
        uniqueBrowsers.add("Edge");
        uniqueBrowsers.add("Chrome");   // Duplicate - ignored!
        
        System.out.println("Unique browsers: " + uniqueBrowsers);
        System.out.println("Size: " + uniqueBrowsers.size());  // 3, not 5!
        
        // Practical: Finding unique error messages from test runs
        Set<String> uniqueErrors = new HashSet<>();
        uniqueErrors.add("Element not found");
        uniqueErrors.add("Timeout exception");
        uniqueErrors.add("Element not found");  // Duplicate
        uniqueErrors.add("Null pointer exception");
        uniqueErrors.add("Timeout exception");  // Duplicate
        
        System.out.println("\nUnique errors (" + uniqueErrors.size() + "):");
        for (String error : uniqueErrors) {
            System.out.println("  - " + error);
        }
        
        // Set operations
        Set<String> set1 = new HashSet<>(Set.of("A", "B", "C", "D"));
        Set<String> set2 = new HashSet<>(Set.of("C", "D", "E", "F"));
        
        // Union
        Set<String> union = new HashSet<>(set1);
        union.addAll(set2);
        System.out.println("\nUnion: " + union);
        
        // Intersection
        Set<String> intersection = new HashSet<>(set1);
        intersection.retainAll(set2);
        System.out.println("Intersection: " + intersection);
        
        // Difference
        Set<String> difference = new HashSet<>(set1);
        difference.removeAll(set2);
        System.out.println("Difference (set1 - set2): " + difference);
    }
}
```

---

## Chapter 23: Generics

### Theory:
Generics enable you to write **type-safe, reusable code** that works with different data types. The type is specified when you use the class/method, not when you write it. Think of it as a template.

```java
// ═══════════════════════════════════════
// GENERIC CLASS
// ═══════════════════════════════════════

// T is a type parameter - placeholder for any type
public class TestResult<T> {
    private String testName;
    private T result;
    private boolean passed;
    
    public TestResult(String testName, T result, boolean passed) {
        this.testName = testName;
        this.result = result;
        this.passed = passed;
    }
    
    public T getResult() { return result; }
    public String getTestName() { return testName; }
    public boolean isPassed() { return passed; }
    
    @Override
    public String toString() {
        return testName + ": " + (passed ? "PASS" : "FAIL") + " - Result: " + result;
    }
}

// ═══════════════════════════════════════
// GENERIC METHOD
// ═══════════════════════════════════════

public class GenericUtils {
    
    // Generic method - works with any type
    public static <T> void printArray(T[] array) {
        for (T element : array) {
            System.out.print(element + " ");
        }
        System.out.println();
    }
    
    // Bounded generic - T must be Comparable
    public static <T extends Comparable<T>> T findMax(T[] array) {
        T max = array[0];
        for (T element : array) {
            if (element.compareTo(max) > 0) {
                max = element;
            }
        }
        return max;
    }
    
    // Multiple type parameters
    public static <K, V> void printKeyValue(K key, V value) {
        System.out.println("Key: " + key + ", Value: " + value);
    }
    
    public static void main(String[] args) {
        // Using generic class with different types
        TestResult<String> stringResult = new TestResult<>("Login Test", "Success", true);
        TestResult<Integer> intResult = new TestResult<>("Score Test", 95, true);
        TestResult<Double> doubleResult = new TestResult<>("Performance", 2.5, true);
        
        System.out.println(stringResult);
        System.out.println(intResult);
        System.out.println(doubleResult);
        
        // Using generic methods
        Integer[] numbers = {1, 5, 3, 9, 2};
        String[] words = {"banana", "apple", "cherry"};
        
        printArray(numbers);
        printArray(words);
        
        System.out.println("Max number: " + findMax(numbers));
        System.out.println("Max word: " + findMax(words));
        
        printKeyValue("browser", "chrome");
        printKeyValue(1, true);
    }
}
```

---

## Chapter 24: Java 8+ Features (Lambda & Streams)

### Theory:
Java 8 introduced **functional programming** features that make code more concise and expressive. These are widely used in modern automation frameworks.

```java
import java.util.*;
import java.util.stream.*;
import java.util.function.*;

public class Java8Features {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // 1. LAMBDA EXPRESSIONS
        // Short way to write anonymous functions
        // Syntax: (parameters) -> expression
        //    or:  (parameters) -> { statements; }
        // ═══════════════════════════════════════
        
        System.out.println("=== Lambda Expressions ===");
        
        // Before Java 8: Anonymous inner class
        Runnable oldWay = new Runnable() {
            @Override
            public void run() {
                System.out.println("Old way - verbose!");
            }
        };
        
        // After Java 8: Lambda expression
        Runnable newWay = () -> System.out.println("Lambda way - concise!");
        
        oldWay.run();
        newWay.run();
        
        // Sorting with Lambda
        List<String> names = new ArrayList<>(Arrays.asList("Charlie", "Alice", "Bob"));
        
        // Old way
        // Collections.sort(names, new Comparator<String>() {
        //     public int compare(String a, String b) {
        //         return a.compareTo(b);
        //     }
        // });
        
        // Lambda way
        Collections.sort(names, (a, b) -> a.compareTo(b));
        // Or even shorter:
        names.sort(String::compareTo);  // Method reference
        
        System.out.println("Sorted: " + names);
        
        
        // ═══════════════════════════════════════
        // 2. FUNCTIONAL INTERFACES
        // Interface with exactly ONE abstract method
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Functional Interfaces ===");
        
        // Predicate: takes input, returns boolean
        Predicate<String> isLongEnough = s -> s.length() >= 5;
        System.out.println("'Hello' is long enough: " + isLongEnough.test("Hello"));
        System.out.println("'Hi' is long enough: " + isLongEnough.test("Hi"));
        
        // Function: takes input, returns output
        Function<String, Integer> getLength = s -> s.length();
        System.out.println("Length of 'Hello': " + getLength.apply("Hello"));
        
        // Consumer: takes input, returns nothing (void)
        Consumer<String> printer = s -> System.out.println(">> " + s);
        printer.accept("Hello from Consumer!");
        
        // Supplier: takes nothing, returns output
        Supplier<String> getTimestamp = () -> new java.util.Date().toString();
        System.out.println("Time: " + getTimestamp.get());
        
        
        // ═══════════════════════════════════════
        // 3. STREAMS API
        // Process collections in a functional way
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Streams API ===");
        
        List<String> testCases = Arrays.asList(
            "Login Test", "Search Test", "Checkout Test",
            "Payment Test", "Login Negative Test", "Search Advanced Test"
        );
        
        // Filter: Keep only elements matching a condition
        System.out.println("Login-related tests:");
        testCases.stream()
                 .filter(test -> test.contains("Login"))
                 .forEach(test -> System.out.println("  " + test));
        
        // Map: Transform each element
        System.out.println("\nUppercase test names:");
        List<String> upperNames = testCases.stream()
                                           .map(String::toUpperCase)
                                           .collect(Collectors.toList());
        upperNames.forEach(System.out::println);
        
        // Count
        long loginTestCount = testCases.stream()
                                       .filter(t -> t.contains("Login"))
                                       .count();
        System.out.println("\nLogin test count: " + loginTestCount);
        
        // Chaining operations
        System.out.println("\nSorted, filtered, and transformed:");
        testCases.stream()
                 .filter(t -> t.contains("Test"))
                 .sorted()
                 .map(t -> "✅ " + t)
                 .forEach(System.out::println);
        
        // Working with numbers
        List<Integer> scores = Arrays.asList(85, 92, 78, 95, 88, 76, 98, 70);
        
        int sum = scores.stream().mapToInt(Integer::intValue).sum();
        double avg = scores.stream().mapToInt(Integer::intValue).average().orElse(0);
        int max = scores.stream().mapToInt(Integer::intValue).max().orElse(0);
        int min = scores.stream().mapToInt(Integer::intValue).min().orElse(0);
        
        System.out.println("\nScore Statistics:");
        System.out.println("Sum: " + sum);
        System.out.println("Average: " + avg);
        System.out.println("Max: " + max);
        System.out.println("Min: " + min);
        
        // Collect to different collections
        List<Integer> passingScores = scores.stream()
                                            .filter(s -> s >= 80)
                                            .sorted()
                                            .collect(Collectors.toList());
        System.out.println("Passing scores: " + passingScores);
        
        // Joining strings
        String allTests = testCases.stream()
                                   .collect(Collectors.joining(", "));
        System.out.println("\nAll tests: " + allTests);
        
        // Grouping
        Map<Boolean, List<Integer>> grouped = scores.stream()
            .collect(Collectors.partitioningBy(s -> s >= 80));
        System.out.println("Passing: " + grouped.get(true));
        System.out.println("Failing: " + grouped.get(false));
        
        // AnyMatch, AllMatch, NoneMatch
        boolean anyFailed = scores.stream().anyMatch(s -> s < 60);
        boolean allPassed = scores.stream().allMatch(s -> s >= 60);
        boolean nonePerfect = scores.stream().noneMatch(s -> s == 100);
        
        System.out.println("\nAny failed (<60): " + anyFailed);
        System.out.println("All passed (>=60): " + allPassed);
        System.out.println("None perfect (100): " + nonePerfect);
        
        
        // ═══════════════════════════════════════
        // 4. OPTIONAL (Handle null safely)
        // ═══════════════════════════════════════
        
        System.out.println("\n=== Optional ===");
        
        Optional<String> optionalName = Optional.of("John");
        Optional<String> emptyOptional = Optional.empty();
        Optional<String> nullableOpt = Optional.ofNullable(null);
        
        // Safe access
        System.out.println("Has value: " + optionalName.isPresent());  // true
        System.out.println("Value: " + optionalName.get());
        
        // Default value if absent
        String name = emptyOptional.orElse("Default Name");
        System.out.println("Name: " + name);
        
        // Do something if present
        optionalName.ifPresent(n -> System.out.println("Hello, " + n + "!"));
    }
}
```

---

## Chapter 25: File Handling

### Theory:
Reading from and writing to files is essential in testing for:
- Reading test data (CSV, text files)
- Writing test reports
- Reading configuration files
- Logging test results

```java
import java.io.*;
import java.nio.file.*;
import java.util.*;

public class FileHandling {
    public static void main(String[] args) {
        
        // ═══════════════════════════════════════
        // 1. WRITING TO A FILE
        // ═══════════════════════════════════════
        
        // Using BufferedWriter (traditional)
        try (BufferedWriter writer = new BufferedWriter(new FileWriter("test_results.txt"))) {
            writer.write("Test Execution Report");
            writer.newLine();
            writer.write("====================");
            writer.newLine();
            writer.write("Login Test: PASS");
            writer.newLine();
            writer.write("Search Test: FAIL");
            writer.newLine();
            writer.write("Checkout Test: PASS");
            System.out.println("✅ File written successfully!");
        } catch (IOException e) {
            System.out.println("❌ Error writing file: " + e.getMessage());
        }
        
        // Using Files class (modern way - Java 7+)
        try {
            List<String> lines = Arrays.asList(
                "username,password,expected",
                "admin,admin123,success",
                "user,user123,success",
                "admin,wrong,failure"
            );
            Files.write(Paths.get("test_data.csv"), lines);
            System.out.println("✅ CSV file created!");
        } catch (IOException e) {
            System.out.println("❌ Error: " + e.getMessage());
        }
        
        
        // ═══════════════════════════════════════
        // 2. READING FROM A FILE
        // ═══════════════════════════════════════
        
        System.out.println("\n--- Reading File ---");
        
        // Using BufferedReader
        try (BufferedReader reader = new BufferedReader(new FileReader("test_results.txt"))) {
            String line;
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
        } catch (IOException e) {
            System.out.println("❌ Error reading file: " + e.getMessage());
        }
        
        // Using Files class (reads all lines at once)
        try {
            List<String> allLines = Files.readAllLines(Paths.get("test_data.csv"));
            System.out.println("\n--- CSV Data ---");
            for (String line : allLines) {
                System.out.println(line);
            }
        } catch (IOException e) {
            System.out.println("❌ Error: " + e.getMessage());
        }
        
        
        // ═══════════════════════════════════════
        // 3. READING CSV FOR TEST DATA
        // ═══════════════════════════════════════
        
        System.out.println("\n--- Parsing CSV Test Data ---");
        try {
            List<String> lines = Files.readAllLines(Paths.get("test_data.csv"));
            
            // Skip header row
            for (int i = 1; i < lines.size(); i++) {
                String[] fields = lines.get(i).split(",");
                String username = fields[0];
                String password = fields[1];
                String expected = fields[2];
                
                System.out.printf("Test %d: Login with user='%s', pass='%s', expect='%s'%n",
                    i, username, password, expected);
            }
        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }
        
        
        // ═══════════════════════════════════════
        // 4. PROPERTIES FILES (Key-Value config)
        // ═══════════════════════════════════════
        
        // Create properties file
        try {
            Properties props = new Properties();
            props.setProperty("browser", "chrome");
            props.setProperty("baseUrl", "https://www.example.com");
            props.setProperty("implicitWait", "10");
            props.setProperty("headless", "false");
            
            try (FileOutputStream fos = new FileOutputStream("config.properties")) {
                props.store(fos, "Test Configuration");
            }
            System.out.println("\n✅ Properties file created!");
            
            // Read properties file
            Properties readProps = new Properties();
            try (FileInputStream fis = new FileInputStream("config.properties")) {
                readProps.load(fis);
            }
            
            System.out.println("Browser: " + readProps.getProperty("browser"));
            System.out.println("URL: " + readProps.getProperty("baseUrl"));
            System.out.println("Wait: " + readProps.getProperty("implicitWait"));
            
        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }
        
        
        // ═══════════════════════════════════════
        // 5. FILE OPERATIONS
        // ═══════════════════════════════════════
        
        File file = new File("test_results.txt");
        System.out.println("\nFile exists: " + file.exists());
        System.out.println("File name: " + file.getName());
        System.out.println("File size: " + file.length() + " bytes");
        System.out.println("Can read: " + file.canRead());
        System.out.println("Absolute path: " + file.getAbsolutePath());
        
        // Create directory
        File dir = new File("test-output");
        if (!dir.exists()) {
            boolean created = dir.mkdirs();
            System.out.println("Directory created: " + created);
        }
        
        // List files in directory
        File currentDir = new File(".");
        File[] files = currentDir.listFiles();
        if (files != null) {
            System.out.println("\nFiles in current directory:");
            for (File f : files) {
                System.out.println("  " + (f.isDirectory() ? "[DIR] " : "[FILE] ") + f.getName());
            }
        }
    }
}
```

---

## Chapter 26: Date and Time API

```java
import java.time.*;
import java.time.format.DateTimeFormatter;

public class DateTimeDemo {
    public static void main(String[] args) {
        
        // Current date and time
        LocalDate today = LocalDate.now();
        LocalTime now = LocalTime.now();
        LocalDateTime dateTime = LocalDateTime.now();
        
        System.out.println("Date: " + today);
        System.out.println("Time: " + now);
        System.out.println("DateTime: " + dateTime);
        
        // Formatting (for reports and logs)
        DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");
        String formatted = dateTime.format(formatter);
        System.out.println("Formatted: " + formatted);
        
        // For screenshot names
        DateTimeFormatter fileFormatter = DateTimeFormatter.ofPattern("yyyyMMdd_HHmmss");
        String screenshotName = "screenshot_" + dateTime.format(fileFormatter) + ".png";
        System.out.println("Screenshot: " + screenshotName);
        
        // Measuring execution time
        long startTime = System.currentTimeMillis();
        // ... some operation
        try { Thread.sleep(1000); } catch (InterruptedException e) {}
        long endTime = System.currentTimeMillis();
        System.out.println("Execution time: " + (endTime - startTime) + " ms");
    }
}
```

---

---

# 📕 PHASE 4: ADVANCED JAVA (Weeks 13-16)

---

## Chapter 27: Design Patterns (Essential for Testing)

### Theory:
Design patterns are proven solutions to common problems in software design. In automation testing, specific patterns are crucial for building maintainable frameworks.

### 1. Singleton Pattern:
```java
// ═══════════════════════════════════════
// SINGLETON: Only ONE instance exists
// Use: WebDriver manager, Config reader, Logger
// ═══════════════════════════════════════

public class DriverManager {
    // Private static instance
    private static DriverManager instance;
    
    // The driver (simulated)
    private String driver;
    
    // Private constructor - prevents external instantiation
    private DriverManager() {
        System.out.println("DriverManager created - initializing driver...");
        this.driver = "ChromeDriver instance";
    }
    
    // Public access method
    public static DriverManager getInstance() {
        if (instance == null) {
            synchronized (DriverManager.class) {  // Thread-safe
                if (instance == null) {
                    instance = new DriverManager();
                }
            }
        }
        return instance;
    }
    
    public String getDriver() {
        return driver;
    }
    
    public void quitDriver() {
        System.out.println("Quitting driver...");
        driver = null;
        instance = null;
    }
}

// Usage:
// DriverManager dm1 = DriverManager.getInstance();
// DriverManager dm2 = DriverManager.getInstance();
// System.out.println(dm1 == dm2);  // true - same instance!
```

### 2. Factory Pattern:
```java
// ═══════════════════════════════════════
// FACTORY: Creates objects without exposing creation logic
// Use: Creating different browser drivers
// ═══════════════════════════════════════

// Product interface
interface WebDriver {
    void get(String url);
    String getTitle();
    void quit();
}

class ChromeDriver implements WebDriver {
    public ChromeDriver() { System.out.println("Chrome browser launched"); }
    public void get(String url) { System.out.println("Chrome navigating to: " + url); }
    public String getTitle() { return "Chrome - Page Title"; }
    public void quit() { System.out.println("Chrome closed"); }
}

class FirefoxDriver implements WebDriver {
    public FirefoxDriver() { System.out.println("Firefox browser launched"); }
    public void get(String url) { System.out.println("Firefox navigating to: " + url); }
    public String getTitle() { return "Firefox - Page Title"; }
    public void quit() { System.out.println("Firefox closed"); }
}

class EdgeDriver implements WebDriver {
    public EdgeDriver() { System.out.println("Edge browser launched"); }
    public void get(String url) { System.out.println("Edge navigating to: " + url); }
    public String getTitle() { return "Edge - Page Title"; }
    public void quit() { System.out.println("Edge closed"); }
}

// Factory class
class WebDriverFactory {
    public static WebDriver createDriver(String browserName) {
        switch (browserName.toLowerCase()) {
            case "chrome":
                return new ChromeDriver();
            case "firefox":
                return new FirefoxDriver();
            case "edge":
                return new EdgeDriver();
            default:
                throw new IllegalArgumentException("Unsupported browser: " + browserName);
        }
    }
}

// Usage:
// WebDriver driver = WebDriverFactory.createDriver("chrome");
// driver.get("https://www.google.com");
// driver.quit();
```

### 3. Page Object Model (Preview):
```java
// ═══════════════════════════════════════
// PAGE OBJECT MODEL: Each page = one class
// Separates test logic from page interaction logic
// ═══════════════════════════════════════

class BasePage {
    protected WebDriver driver;
    
    public BasePage(WebDriver driver) {
        this.driver = driver;
    }
    
    protected void click(String locator) {
        System.out.println("Clicking: " + locator);
    }
    
    protected void type(String locator, String text) {
        System.out.println("Typing '" + text + "' in: " + locator);
    }
    
    protected String getText(String locator) {
        System.out.println("Getting text from: " + locator);
        return "Sample Text";
    }
}

class LoginPage extends BasePage {
    // Locators
    private String usernameField = "#username";
    private String passwordField = "#password";
    private String loginButton = "#loginBtn";
    private String errorMessage = ".error-msg";
    
    public LoginPage(WebDriver driver) {
        super(driver);
    }
    
    // Page Actions
    public void enterUsername(String username) {
        type(usernameField, username);
    }
    
    public void enterPassword(String password) {
        type(passwordField, password);
    }
    
    public HomePage clickLogin() {
        click(loginButton);
        return new HomePage(driver);  // Returns next page
    }
    
    // Composite action
    public HomePage loginAs(String username, String password) {
        enterUsername(username);
        enterPassword(password);
        return clickLogin();
    }
    
    public String getErrorMessage() {
        return getText(errorMessage);
    }
}

class HomePage extends BasePage {
    private String welcomeMessage = "#welcome";
    private String logoutButton = "#logout";
    
    public HomePage(WebDriver driver) {
        super(driver);
    }
    
    public String getWelcomeMessage() {
        return getText(welcomeMessage);
    }
    
    public LoginPage logout() {
        click(logoutButton);
        return new LoginPage(driver);
    }
}
```

---

## Chapter 28: Multithreading Basics

### Theory:
Multithreading allows multiple parts of a program to run simultaneously. In testing, this is used for:
- Parallel test execution
- Handling timeouts
- Running tests in multiple browsers simultaneously

```java
// ═══════════════════════════════════════
// 1. Creating Threads
// ═══════════════════════════════════════

// Method 1: Extend Thread class
class TestThread extends Thread {
    private String testName;
    
    public TestThread(String testName) {
        this.testName = testName;
    }
    
    @Override
    public void run() {
        System.out.println(testName + " started on thread: " + Thread.currentThread().getName());
        try {
            Thread.sleep(2000);  // Simulate test execution
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        System.out.println(testName + " completed!");
    }
}

// Method 2: Implement Runnable interface (PREFERRED)
class TestRunnable implements Runnable {
    private String testName;
    
    public TestRunnable(String testName) {
        this.testName = testName;
    }
    
    @Override
    public void run() {
        System.out.println(testName + " started on thread: " + Thread.currentThread().getName());
        try {
            Thread.sleep(1500);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        System.out.println(testName + " completed!");
    }
}

public class MultithreadingDemo {
    public static void main(String[] args) {
        
        System.out.println("=== Sequential Execution ===");
        long start = System.currentTimeMillis();
        
        // Sequential - one after another
        // runTest("Login Test");
        // runTest("Search Test");
        // runTest("Checkout Test");
        
        System.out.println("\n=== Parallel Execution ===");
        
        // Parallel - all at once
        Thread t1 = new TestThread("Login Test");
        Thread t2 = new TestThread("Search Test");
        Thread t3 = new TestThread("Checkout Test");
        
        t1.start();  // start() creates new thread and calls run()
        t2.start();
        t3.start();
        
        // Wait for all threads to complete
        try {
            t1.join();
            t2.join();
            t3.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        
        long end = System.currentTimeMillis();
        System.out.println("Total time: " + (end - start) + " ms");
        
        // Using Runnable with Lambda
        Thread t4 = new Thread(() -> {
            System.out.println("Lambda thread running!");
        });
        t4.start();
    }
}
```

---

## Chapter 29: Maven Basics

### Theory:
**Maven** is a build automation and dependency management tool. It:
- Manages project dependencies (libraries)
- Standardizes project structure
- Builds and packages your project
- Runs tests

### Maven Project Structure:
```
my-project/
├── pom.xml                    ← Project configuration (dependencies, plugins)
├── src/
│   ├── main/
│   │   ├── java/              ← Application source code
│   │   └── resources/         ← Config files, properties
│   └── test/
│       ├── java/              ← Test source code
│       └── resources/         ← Test data, test config
└── target/                    ← Compiled code, reports (auto-generated)
```

### Sample pom.xml:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 
         http://maven.apache.org/xsd/maven-4.0.0.xsd">
    
    <modelVersion>4.0.0</modelVersion>
    
    <!-- Project identity -->
    <groupId>com.mycompany</groupId>
    <artifactId>automation-framework</artifactId>
    <version>1.0-SNAPSHOT</version>
    
    <!-- Properties -->
    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
        <selenium.version>4.15.0</selenium.version>
        <testng.version>7.8.0</testng.version>
    </properties>
    
    <!-- Dependencies (libraries) -->
    <dependencies>
        <!-- Selenium WebDriver -->
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-java</artifactId>
            <version>${selenium.version}</version>
        </dependency>
        
        <!-- TestNG Testing Framework -->
        <dependency>
            <groupId>org.testng</groupId>
            <artifactId>testng</artifactId>
            <version>${testng.version}</version>
            <scope>test</scope>
        </dependency>
        
        <!-- WebDriver Manager -->
        <dependency>
            <groupId>io.github.bonigarcia</groupId>
            <artifactId>webdrivermanager</artifactId>
            <version>5.6.2</version>
        </dependency>
    </dependencies>
</project>
```

### Maven Commands:
```bash
mvn clean            # Delete target folder
mvn compile          # Compile source code
mvn test             # Run tests
mvn package          # Create JAR/WAR
mvn clean test       # Clean and run tests
mvn install          # Install to local repository
```

---

---

# 📘 PHASE 5: AUTOMATION TESTING FOUNDATIONS (Weeks 17-20)

---

## Chapter 30: TestNG Framework

### Theory:
**TestNG** (Test Next Generation) is the most popular testing framework for Java automation. It provides:
- Test annotations and organization
- Test grouping, prioritization, and parameterization
- Parallel execution
- Reporting
- Data-driven testing support

```java
import org.testng.annotations.*;
import org.testng.Assert;

// ═══════════════════════════════════════
// TestNG Test Class
// ═══════════════════════════════════════

public class LoginTests {
    
    // ═══════════════════════════════════════
    // ANNOTATIONS - Control test lifecycle
    // ═══════════════════════════════════════
    
    @BeforeSuite
    public void beforeSuite() {
        System.out.println("⚙️ Before Suite: Setup test environment");
        // Configure logging, read global config
    }
    
    @BeforeClass
    public void beforeClass() {
        System.out.println("⚙️ Before Class: Setup for LoginTests class");
        // Initialize shared resources for this class
    }
    
    @BeforeMethod
    public void setUp() {
        System.out.println("\n⚙️ Before Method: Open browser, navigate to login page");
        // driver = new ChromeDriver();
        // driver.get("https://app.example.com/login");
    }
    
    @AfterMethod
    public void tearDown() {
        System.out.println("⚙️ After Method: Close browser");
        // driver.quit();
    }
    
    @AfterClass
    public void afterClass() {
        System.out.println("⚙️ After Class: Cleanup for LoginTests class");
    }
    
    @AfterSuite
    public void afterSuite() {
        System.out.println("⚙️ After Suite: Final cleanup");
    }
    
    // ═══════════════════════════════════════
    // TEST METHODS
    // ═══════════════════════════════════════
    
    @Test(priority = 1, description = "Verify successful login with valid credentials")
    public void testValidLogin() {
        System.out.println("🧪 Running: testValidLogin");
        
        String username = "admin";
        String password = "admin123";
        
        // Simulate login
        System.out.println("   Entering username: " + username);
        System.out.println("   Entering password: ****");
        System.out.println("   Clicking login button");
        
        // Assertions
        String expectedTitle = "Dashboard";
        String actualTitle = "Dashboard"; // In real test: driver.getTitle()
        
        Assert.assertEquals(actualTitle, expectedTitle, "Page title mismatch!");
        System.out.println("   ✅ Login successful!");
    }
    
    @Test(priority = 2, description = "Verify error message with invalid credentials")
    public void testInvalidLogin() {
        System.out.println("🧪 Running: testInvalidLogin");
        
        // Simulate invalid login
        String expectedError = "Invalid credentials";
        String actualError = "Invalid credentials";
        
        Assert.assertEquals(actualError, expectedError);
        System.out.println("   ✅ Error message displayed correctly!");
    }
    
    @Test(priority = 3, enabled = false)  // Skipped test
    public void testSkippedTest() {
        System.out.println("This won't run because enabled = false");
    }
    
    @Test(priority = 4, groups = {"smoke", "regression"})
    public void testLoginButtonVisible() {
        System.out.println("🧪 Running: testLoginButtonVisible");
        boolean isVisible = true;
        Assert.assertTrue(isVisible, "Login button should be visible");
    }
    
    @Test(priority = 5, dependsOnMethods = {"testValidLogin"})
    public void testDashboardAfterLogin() {
        System.out.println("🧪 Running: testDashboardAfterLogin");
        System.out.println("   This runs only if testValidLogin passes!");
    }
    
    @Test(expectedExceptions = ArithmeticException.class)
    public void testExpectedException() {
        int result = 10 / 0;  // This should throw ArithmeticException
    }
    
    @Test(timeOut = 5000)  // Fails if takes more than 5 seconds
    public void testWithTimeout() {
        System.out.println("🧪 Running: testWithTimeout");
        // Long operation here
    }
    
    // ═══════════════════════════════════════
    // DATA-DRIVEN TESTING with @DataProvider
    // ═══════════════════════════════════════
    
    @DataProvider(name = "loginData")
    public Object[][] getLoginData() {
        return new Object[][] {
            {"admin", "admin123", true},
            {"user", "user123", true},
            {"admin", "wrongpass", false},
            {"", "", false},
            {"admin", "", false},
        };
    }
    
    @Test(dataProvider = "loginData", priority = 10)
    public void testLoginWithMultipleData(String username, String password, boolean expectedResult) {
        System.out.println("🧪 Login attempt: user=" + username + ", expected=" + expectedResult);
        
        // Simulate login
        boolean actualResult;
        if (username.equals("admin") && password.equals("admin123")) {
            actualResult = true;
        } else if (username.equals("user") && password.equals("user123")) {
            actualResult = true;
        } else {
            actualResult = false;
        }
        
        Assert.assertEquals(actualResult, expectedResult,
            "Login result mismatch for user: " + username);
    }
}

// ═══════════════════════════════════════
// ASSERTIONS - Verifying test results
// ═══════════════════════════════════════

class AssertionsDemo {
    @Test
    public void demonstrateAssertions() {
        // Hard Assertions (test stops on first failure)
        Assert.assertEquals("actual", "actual", "Values should match");
        Assert.assertNotEquals("a", "b", "Values should not match");
        Assert.assertTrue(5 > 3, "5 should be greater than 3");
        Assert.assertFalse(5 < 3, "5 is not less than 3");
        Assert.assertNull(null, "Should be null");
        Assert.assertNotNull("hello", "Should not be null");
        
        // Soft Assertions (collects all failures, reports at end)
        org.testng.asserts.SoftAssert softAssert = new org.testng.asserts.SoftAssert();
        softAssert.assertEquals("actual", "expected", "First check");   // Fails but continues
        softAssert.assertTrue(true, "Second check");                     // Passes
        softAssert.assertEquals(10, 10, "Third check");                 // Passes
        softAssert.assertAll();  // Reports all failures at once
    }
}
```

### TestNG XML Configuration (testng.xml):
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE suite SYSTEM "https://testng.org/testng-1.0.dtd">

<suite name="Automation Test Suite" parallel="methods" thread-count="3">
    
    <test name="Smoke Tests">
        <groups>
            <run>
                <include name="smoke"/>
            </run>
        </groups>
        <classes>
            <class name="tests.LoginTests"/>
            <class name="tests.HomePageTests"/>
        </classes>
    </test>
    
    <test name="Regression Tests">
        <classes>
            <class name="tests.LoginTests"/>
            <class name="tests.SearchTests"/>
            <class name="tests.CheckoutTests"/>
        </classes>
    </test>
    
</suite>
```

---

## Chapter 31: Selenium WebDriver

### Theory:
**Selenium WebDriver** is the most popular tool for automating web browser interactions. It supports multiple browsers and programming languages.

```java
import org.openqa.selenium.*;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;
import org.openqa.selenium.support.ui.*;
import io.github.bonigarcia.wdm.WebDriverManager;

import java.time.Duration;

public class SeleniumBasics {
    
    WebDriver driver;
    
    // ═══════════════════════════════════════
    // 1. SETUP & NAVIGATION
    // ═══════════════════════════════════════
    
    public void setUp() {
        // Auto-manage driver binary
        WebDriverManager.chromedriver().setup();
        
        // Chrome options
        ChromeOptions options = new ChromeOptions();
        options.addArguments("--start-maximized");
        // options.addArguments("--headless");  // Run without browser UI
        
        // Create driver instance
        driver = new ChromeDriver(options);
        
        // Set timeouts
        driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
        driver.manage().timeouts().pageLoadTimeout(Duration.ofSeconds(30));
        
        // Maximize window
        driver.manage().window().maximize();
    }
    
    // ═══════════════════════════════════════
    // 2. NAVIGATION
    // ═══════════════════════════════════════
    
    public void navigationDemo() {
        driver.get("https://www.google.com");           // Navigate to URL
        driver.navigate().to("https://www.yahoo.com");  // Navigate to URL
        driver.navigate().back();                        // Go back
        driver.navigate().forward();                     // Go forward
        driver.navigate().refresh();                     // Refresh page
        
        // Get info
        String title = driver.getTitle();
        String url = driver.getCurrentUrl();
        String source = driver.getPageSource();
    }
    
    // ═══════════════════════════════════════
    // 3. LOCATING ELEMENTS
    // ═══════════════════════════════════════
    
    public void locatorDemo() {
        // Single element finders
        WebElement byId = driver.findElement(By.id("username"));
        WebElement byName = driver.findElement(By.name("email"));
        WebElement byClass = driver.findElement(By.className("login-btn"));
        WebElement byTag = driver.findElement(By.tagName("h1"));
        WebElement byLink = driver.findElement(By.linkText("Sign Up"));
        WebElement byPartialLink = driver.findElement(By.partialLinkText("Sign"));
        WebElement byCss = driver.findElement(By.cssSelector("#login-form .btn-primary"));
        WebElement byXpath = driver.findElement(By.xpath("//input[@type='submit']"));
        
        // Multiple elements
        java.util.List<WebElement> allLinks = driver.findElements(By.tagName("a"));
        System.out.println("Total links: " + allLinks.size());
        
        for (WebElement link : allLinks) {
            System.out.println(link.getText() + " → " + link.getAttribute("href"));
        }
    }
    
    // ═══════════════════════════════════════
    // 4. ELEMENT INTERACTIONS
    // ═══════════════════════════════════════
    
    public void interactionDemo() {
        // Text input
        WebElement usernameField = driver.findElement(By.id("username"));
        usernameField.clear();                    // Clear existing text
        usernameField.sendKeys("admin");          // Type text
        usernameField.sendKeys(Keys.TAB);         // Press Tab key
        
        // Clicking
        WebElement loginBtn = driver.findElement(By.id("loginBtn"));
        loginBtn.click();
        
        // Getting element info
        String text = loginBtn.getText();
        String value = usernameField.getAttribute("value");
        String cssValue = loginBtn.getCssValue("background-color");
        boolean isDisplayed = loginBtn.isDisplayed();
        boolean isEnabled = loginBtn.isEnabled();
        boolean isSelected = driver.findElement(By.id("checkbox")).isSelected();
        
        // Submit form
        // usernameField.submit();
    }
    
    // ═══════════════════════════════════════
    // 5. WAITS (Critical for stable tests!)
    // ═══════════════════════════════════════
    
    public void waitDemo() {
        // Implicit Wait: Set once, applies to all findElement calls
        driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
        
        // Explicit Wait: Wait for specific condition
        WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(15));
        
        // Wait until element is visible
        WebElement element = wait.until(
            ExpectedConditions.visibilityOfElementLocated(By.id("result"))
        );
        
        // Wait until element is clickable
        WebElement button = wait.until(
            ExpectedConditions.elementToBeClickable(By.id("submitBtn"))
        );
        
        // Wait until title contains text
        wait.until(ExpectedConditions.titleContains("Dashboard"));
        
        // Wait until element is present in DOM
        wait.until(ExpectedConditions.presenceOfElementLocated(By.id("element")));
        
        // Wait until element disappears
        wait.until(ExpectedConditions.invisibilityOfElementLocated(By.id("loader")));
        
        // Wait until alert is present
        // wait.until(ExpectedConditions.alertIsPresent());
        
        // Fluent Wait: Customizable polling
        Wait<WebDriver> fluentWait = new FluentWait<>(driver)
            .withTimeout(Duration.ofSeconds(30))
            .pollingEvery(Duration.ofMillis(500))
            .ignoring(NoSuchElementException.class)
            .withMessage("Element was not found");
        
        WebElement fluentElement = fluentWait.until(
            d -> d.findElement(By.id("dynamicElement"))
        );
    }
    
    // ═══════════════════════════════════════
    // 6. HANDLING DROPDOWNS
    // ═══════════════════════════════════════
    
    public void dropdownDemo() {
        WebElement dropdown = driver.findElement(By.id("country"));
        Select select = new Select(dropdown);
        
        select.selectByVisibleText("India");
        select.selectByValue("IN");
        select.selectByIndex(2);
        
        // Get selected option
        String selected = select.getFirstSelectedOption().getText();
        
        // Get all options
        java.util.List<WebElement> options = select.getOptions();
        for (WebElement option : options) {
            System.out.println(option.getText());
        }
    }
    
    // ═══════════════════════════════════════
    // 7. HANDLING ALERTS
    // ═══════════════════════════════════════
    
    public void alertDemo() {
        Alert alert = driver.switchTo().alert();
        String alertText = alert.getText();
        alert.accept();     // Click OK
        // alert.dismiss();   // Click Cancel
        // alert.sendKeys("text");  // Type in prompt
    }
    
    // ═══════════════════════════════════════
    // 8. HANDLING FRAMES & WINDOWS
    // ═══════════════════════════════════════
    
    public void framesAndWindowsDemo() {
        // Frames
        driver.switchTo().frame("frameName");       // By name
        driver.switchTo().frame(0);                  // By index
        driver.switchTo().frame(driver.findElement(By.id("frameId")));  // By element
        driver.switchTo().defaultContent();          // Back to main page
        driver.switchTo().parentFrame();             // Back to parent frame
        
        // Windows
        String mainWindow = driver.getWindowHandle();
        java.util.Set<String> allWindows = driver.getWindowHandles();
        
        for (String window : allWindows) {
            if (!window.equals(mainWindow)) {
                driver.switchTo().window(window);
                System.out.println("Switched to: " + driver.getTitle());
                driver.close();
            }
        }
        driver.switchTo().window(mainWindow);
    }
    
    // ═══════════════════════════════════════
    // 9. SCREENSHOT
    // ═══════════════════════════════════════
    
    public void takeScreenshot(String fileName) {
        TakesScreenshot ts = (TakesScreenshot) driver;
        java.io.File source = ts.getScreenshotAs(OutputType.FILE);
        // Copy file to destination
        // FileUtils.copyFile(source, new File("screenshots/" + fileName + ".png"));
    }
    
    // ═══════════════════════════════════════
    // 10. JAVASCRIPT EXECUTOR
    // ═══════════════════════════════════════
    
    public void jsExecutorDemo() {
        JavascriptExecutor js = (JavascriptExecutor) driver;
        
        // Scroll down
        js.executeScript("window.scrollBy(0, 500)");
        
        // Scroll to element
        WebElement element = driver.findElement(By.id("footer"));
        js.executeScript("arguments[0].scrollIntoView(true);", element);
        
        // Click using JS (when normal click doesn't work)
        js.executeScript("arguments[0].click();", element);
        
        // Get page title
        String title = (String) js.executeScript("return document.title");
        
        // Highlight element (useful for debugging)
        js.executeScript(
            "arguments[0].style.border='3px solid red'", element
        );
    }
    
    // ═══════════════════════════════════════
    // 11. ACTIONS CLASS (Mouse & Keyboard)
    // ═══════════════════════════════════════
    
    public void actionsDemo() {
        org.openqa.selenium.interactions.Actions actions = 
            new org.openqa.selenium.interactions.Actions(driver);
        
        WebElement element = driver.findElement(By.id("menu"));
        
        // Mouse actions
        actions.moveToElement(element).perform();              // Hover
        actions.doubleClick(element).perform();                // Double click
        actions.contextClick(element).perform();               // Right click
        
        // Drag and drop
        WebElement source = driver.findElement(By.id("source"));
        WebElement target = driver.findElement(By.id("target"));
        actions.dragAndDrop(source, target).perform();
        
        // Keyboard actions
        actions.keyDown(Keys.CONTROL)
               .sendKeys("a")
               .keyUp(Keys.CONTROL)
               .perform();  // Ctrl+A (Select All)
    }
    
    // ═══════════════════════════════════════
    // CLEANUP
    // ═══════════════════════════════════════
    
    public void tearDown() {
        if (driver != null) {
            driver.quit();
        }
    }
}
```

---

## Chapter 32: Complete Test Example

```java
import org.openqa.selenium.*;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.*;
import org.testng.Assert;
import org.testng.annotations.*;
import io.github.bonigarcia.wdm.WebDriverManager;
import java.time.Duration;

public class GoogleSearchTest {
    WebDriver driver;
    WebDriverWait wait;
    
    @BeforeMethod
    public void setUp() {
        WebDriverManager.chromedriver().setup();
        driver = new ChromeDriver();
        driver.manage().window().maximize();
        driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
        wait = new WebDriverWait(driver, Duration.ofSeconds(15));
    }
    
    @Test(priority = 1)
    public void testGoogleSearch() {
        // Navigate
        driver.get("https://www.google.com");
        
        // Verify title
        Assert.assertTrue(driver.getTitle().contains("Google"), 
            "Should be on Google homepage");
        
        // Search
        WebElement searchBox = driver.findElement(By.name("q"));
        searchBox.sendKeys("Selenium WebDriver");
        searchBox.sendKeys(Keys.ENTER);
        
        // Wait for results
        wait.until(ExpectedConditions.presenceOfElementLocated(By.id("search")));
        
        // Verify results
        String title = driver.getTitle();
        Assert.assertTrue(title.contains("Selenium WebDriver"),
            "Title should contain search term");
        
        // Count results
        java.util.List<WebElement> results = driver.findElements(
            By.cssSelector("#search .g"));
        Assert.assertTrue(results.size() > 0, "Should have search results");
        
        System.out.println("Found " + results.size() + " results");
        
        // Print first 3 results
        for (int i = 0; i < Math.min(3, results.size()); i++) {
            WebElement result = results.get(i);
            String resultText = result.findElement(By.tagName("h3")).getText();
            System.out.println((i + 1) + ". " + resultText);
        }
    }
    
    @Test(priority = 2)
    public void testGoogleTitle() {
        driver.get("https://www.google.com");
        Assert.assertEquals(driver.getTitle(), "Google");
    }
    
    @AfterMethod
    public void tearDown() {
        if (driver != null) {
            driver.quit();
        }
    }
}
```

---

---

# 📗 PHASE 6: ADVANCED AUTOMATION (Weeks 21-24)

---

## Chapter 33: Page Object Model Framework

### Complete Framework Structure:
```
automation-framework/
├── pom.xml
├── src/
│   ├── main/
│   │   └── java/
│   │       └── com/framework/
│   │           ├── base/
│   │           │   └── BasePage.java
│   │           ├── pages/
│   │           │   ├── LoginPage.java
│   │           │   ├── HomePage.java
│   │           │   └── SearchPage.java
│   │           ├── utils/
│   │           │   ├── ConfigReader.java
│   │           │   ├── ExcelReader.java
│   │           │   ├── WaitUtils.java
│   │           │   └── ScreenshotUtils.java
│   │           └── factory/
│   │               └── DriverFactory.java
│   └── test/
│       ├── java/
│       │   └── com/tests/
│       │       ├── base/
│       │       │   └── BaseTest.java
│       │       ├── LoginTests.java
│       │       ├── HomePageTests.java
│       │       └── SearchTests.java
│       └── resources/
│           ├── config.properties
│           ├── testdata/
│           │   └── loginData.xlsx
│           └── testng.xml
```

### Implementation:

```java
// ═══════════════════════════════════════
// 1. DriverFactory.java
// ═══════════════════════════════════════

package com.framework.factory;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.edge.EdgeDriver;
import io.github.bonigarcia.wdm.WebDriverManager;

public class DriverFactory {
    
    // ThreadLocal for parallel execution
    private static ThreadLocal<WebDriver> tlDriver = new ThreadLocal<>();
    
    public static WebDriver initDriver(String browser) {
        WebDriver driver;
        
        switch (browser.toLowerCase()) {
            case "chrome":
                WebDriverManager.chromedriver().setup();
                ChromeOptions options = new ChromeOptions();
                options.addArguments("--start-maximized");
                driver = new ChromeDriver(options);
                break;
                
            case "firefox":
                WebDriverManager.firefoxdriver().setup();
                driver = new FirefoxDriver();
                break;
                
            case "edge":
                WebDriverManager.edgedriver().setup();
                driver = new EdgeDriver();
                break;
                
            default:
                throw new IllegalArgumentException("Unsupported browser: " + browser);
        }
        
        tlDriver.set(driver);
        return driver;
    }
    
    public static WebDriver getDriver() {
        return tlDriver.get();
    }
    
    public static void quitDriver() {
        if (tlDriver.get() != null) {
            tlDriver.get().quit();
            tlDriver.remove();
        }
    }
}


// ═══════════════════════════════════════
// 2. ConfigReader.java
// ═══════════════════════════════════════

package com.framework.utils;

import java.io.*;
import java.util.Properties;

public class ConfigReader {
    private static Properties properties;
    
    static {
        try {
            FileInputStream fis = new FileInputStream("src/test/resources/config.properties");
            properties = new Properties();
            properties.load(fis);
        } catch (IOException e) {
            throw new RuntimeException("Could not load config file", e);
        }
    }
    
    public static String get(String key) {
        String value = properties.getProperty(key);
        if (value == null) {
            throw new RuntimeException("Property '" + key + "' not found in config");
        }
        return value.trim();
    }
    
    public static String getBrowser() { return get("browser"); }
    public static String getBaseUrl() { return get("baseUrl"); }
    public static int getImplicitWait() { return Integer.parseInt(get("implicitWait")); }
}


// ═══════════════════════════════════════
// 3. BasePage.java
// ═══════════════════════════════════════

package com.framework.base;

import org.openqa.selenium.*;
import org.openqa.selenium.support.ui.*;
import java.time.Duration;

public class BasePage {
    protected WebDriver driver;
    protected WebDriverWait wait;
    
    public BasePage(WebDriver driver) {
        this.driver = driver;
        this.wait = new WebDriverWait(driver, Duration.ofSeconds(15));
    }
    
    // ═══════════════════════════════════════
    // Reusable wrapper methods
    // ═══════════════════════════════════════
    
    protected WebElement waitForElement(By locator) {
        return wait.until(ExpectedConditions.visibilityOfElementLocated(locator));
    }
    
    protected void click(By locator) {
        waitForElement(locator).click();
    }
    
    protected void type(By locator, String text) {
        WebElement element = waitForElement(locator);
        element.clear();
        element.sendKeys(text);
    }
    
    protected String getText(By locator) {
        return waitForElement(locator).getText();
    }
    
    protected boolean isElementDisplayed(By locator) {
        try {
            return waitForElement(locator).isDisplayed();
        } catch (TimeoutException e) {
            return false;
        }
    }
    
    protected void selectDropdown(By locator, String visibleText) {
        Select select = new Select(waitForElement(locator));
        select.selectByVisibleText(visibleText);
    }
    
    protected String getPageTitle() {
        return driver.getTitle();
    }
    
    protected String getCurrentUrl() {
        return driver.getCurrentUrl();
    }
}


// ═══════════════════════════════════════
// 4. LoginPage.java (Page Object)
// ═══════════════════════════════════════

package com.framework.pages;

import com.framework.base.BasePage;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;

public class LoginPage extends BasePage {
    
    // ═══ LOCATORS ═══
    private By usernameField = By.id("username");
    private By passwordField = By.id("password");
    private By loginButton = By.id("loginBtn");
    private By errorMessage = By.cssSelector(".error-message");
    private By forgotPasswordLink = By.linkText("Forgot Password?");
    private By rememberMeCheckbox = By.id("rememberMe");
    
    // ═══ CONSTRUCTOR ═══
    public LoginPage(WebDriver driver) {
        super(driver);
    }
    
    // ═══ PAGE ACTIONS ═══
    public LoginPage enterUsername(String username) {
        type(usernameField, username);
        return this;  // Method chaining (Fluent design)
    }
    
    public LoginPage enterPassword(String password) {
        type(passwordField, password);
        return this;
    }
    
    public HomePage clickLogin() {
        click(loginButton);
        return new HomePage(driver);
    }
    
    // Composite method
    public HomePage loginAs(String username, String password) {
        return enterUsername(username)
                .enterPassword(password)
                .clickLogin();
    }
    
    public LoginPage loginExpectingError(String username, String password) {
        enterUsername(username);
        enterPassword(password);
        click(loginButton);
        return this;
    }
    
    // ═══ GETTERS ═══
    public String getErrorMessage() {
        return getText(errorMessage);
    }
    
    public boolean isErrorDisplayed() {
        return isElementDisplayed(errorMessage);
    }
    
    public boolean isLoginPageDisplayed() {
        return isElementDisplayed(usernameField) && isElementDisplayed(loginButton);
    }
}


// ═══════════════════════════════════════
// 5. HomePage.java (Page Object)
// ═══════════════════════════════════════

package com.framework.pages;

import com.framework.base.BasePage;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;

public class HomePage extends BasePage {
    
    private By welcomeMessage = By.id("welcome");
    private By logoutButton = By.id("logout");
    private By searchBox = By.id("searchInput");
    private By profileLink = By.id("profile");
    
    public HomePage(WebDriver driver) {
        super(driver);
    }
    
    public String getWelcomeMessage() {
        return getText(welcomeMessage);
    }
    
    public boolean isHomePageDisplayed() {
        return isElementDisplayed(welcomeMessage);
    }
    
    public LoginPage logout() {
        click(logoutButton);
        return new LoginPage(driver);
    }
    
    public SearchPage search(String query) {
        type(searchBox, query);
        return new SearchPage(driver);
    }
}


// ═══════════════════════════════════════
// 6. BaseTest.java
// ═══════════════════════════════════════

package com.tests.base;

import com.framework.factory.DriverFactory;
import com.framework.utils.ConfigReader;
import org.openqa.selenium.WebDriver;
import org.testng.annotations.*;
import java.time.Duration;

public class BaseTest {
    protected WebDriver driver;
    
    @BeforeMethod
    public void setUp() {
        String browser = ConfigReader.getBrowser();
        driver = DriverFactory.initDriver(browser);
        driver.manage().timeouts().implicitlyWait(
            Duration.ofSeconds(ConfigReader.getImplicitWait())
        );
        driver.get(ConfigReader.getBaseUrl());
    }
    
    @AfterMethod
    public void tearDown() {
        DriverFactory.quitDriver();
    }
}


// ═══════════════════════════════════════
// 7. LoginTests.java (Test Class)
// ═══════════════════════════════════════

package com.tests;

import com.framework.pages.LoginPage;
import com.framework.pages.HomePage;
import com.tests.base.BaseTest;
import org.testng.Assert;
import org.testng.annotations.*;

public class LoginTests extends BaseTest {
    
    LoginPage loginPage;
    
    @BeforeMethod(dependsOnMethods = "setUp")
    public void initPage() {
        loginPage = new LoginPage(driver);
    }
    
    @Test(priority = 1, description = "Verify login page is displayed")
    public void testLoginPageDisplayed() {
        Assert.assertTrue(loginPage.isLoginPageDisplayed(),
            "Login page should be displayed");
    }
    
    @Test(priority = 2, description = "Verify valid login")
    public void testValidLogin() {
        HomePage homePage = loginPage.loginAs("admin", "admin123");
        
        Assert.assertTrue(homePage.isHomePageDisplayed(),
            "Home page should be displayed after login");
        Assert.assertTrue(homePage.getWelcomeMessage().contains("Welcome"),
            "Welcome message should be displayed");
    }
    
    @Test(priority = 3, description = "Verify invalid login shows error")
    public void testInvalidLogin() {
        loginPage.loginExpectingError("admin", "wrongpassword");
        
        Assert.assertTrue(loginPage.isErrorDisplayed(),
            "Error message should be displayed");
        Assert.assertEquals(loginPage.getErrorMessage(),
            "Invalid credentials",
            "Error message text should match");
    }
    
    @Test(priority = 4, dataProvider = "loginData")
    public void testLoginWithMultipleCredentials(
            String username, String password, String expectedResult) {
        
        if (expectedResult.equals("success")) {
            HomePage homePage = loginPage.loginAs(username, password);
            Assert.assertTrue(homePage.isHomePageDisplayed());
        } else {
            loginPage.loginExpectingError(username, password);
            Assert.assertTrue(loginPage.isErrorDisplayed());
        }
    }
    
    @DataProvider(name = "loginData")
    public Object[][] getLoginData() {
        return new Object[][] {
            {"admin", "admin123", "success"},
            {"user", "user123", "success"},
            {"admin", "wrong", "failure"},
            {"", "", "failure"}
        };
    }
}
```

### config.properties:
```properties
# Browser Configuration
browser=chrome
headless=false

# Application Configuration
baseUrl=https://app.example.com/login

# Wait Configuration
implicitWait=10
explicitWait=15
pageLoadTimeout=30

# Screenshot Configuration
screenshotOnFailure=true
screenshotPath=./test-output/screenshots/
```

---

## Chapter 34: API Testing with Rest Assured (Brief Introduction)

```java
import io.restassured.RestAssured;
import io.restassured.response.Response;
import static io.restassured.RestAssured.*;
import static org.hamcrest.Matchers.*;

public class APITestDemo {
    
    @BeforeClass
    public void setup() {
        RestAssured.baseURI = "https://jsonplaceholder.typicode.com";
    }
    
    @Test
    public void testGetUsers() {
        given()
            .header("Content-Type", "application/json")
        .when()
            .get("/users")
        .then()
            .statusCode(200)
            .body("size()", greaterThan(0))
            .body("[0].name", notNullValue());
    }
    
    @Test
    public void testCreateUser() {
        String requestBody = """
            {
                "name": "John Doe",
                "email": "john@test.com",
                "username": "johndoe"
            }
            """;
        
        Response response = 
            given()
                .header("Content-Type", "application/json")
                .body(requestBody)
            .when()
                .post("/users")
            .then()
                .statusCode(201)
                .body("name", equalTo("John Doe"))
                .extract().response();
        
        System.out.println("Created user ID: " + response.jsonPath().getInt("id"));
    }
}
```

---

## Chapter 35: Reporting with Extent Reports

```java
import com.aventstack.extentreports.*;
import com.aventstack.extentreports.reporter.ExtentSparkReporter;

public class ExtentReportDemo {
    
    static ExtentReports extent;
    static ExtentTest test;
    
    @BeforeSuite
    public void setupReport() {
        ExtentSparkReporter spark = new ExtentSparkReporter("test-output/report.html");
        spark.config().setDocumentTitle("Automation Test Report");
        spark.config().setReportName("Regression Suite Results");
        
        extent = new ExtentReports();
        extent.attachReporter(spark);
        extent.setSystemInfo("OS", System.getProperty("os.name"));
        extent.setSystemInfo("Browser", "Chrome");
        extent.setSystemInfo("Tester", "John Doe");
    }
    
    @Test
    public void testLogin() {
        test = extent.createTest("Login Test", "Verify login functionality");
        
        test.info("Navigating to login page");
        test.info("Entering username: admin");
        test.info("Entering password: ****");
        test.info("Clicking login button");
        
        // After assertion
        test.pass("Login was successful!");
        // OR
        // test.fail("Login failed: " + errorMessage);
        // test.addScreenCaptureFromPath("screenshots/login_failure.png");
    }
    
    @AfterSuite
    public void tearDownReport() {
        extent.flush();
    }
}
```

---

## 📋 COMPLETE LEARNING ROADMAP SUMMARY

```
WEEK 1-4:   Java Basics
             └── Variables, Data Types, Operators
             └── Control Flow (if-else, loops)
             └── Arrays and Strings
             └── Methods

WEEK 5-8:   Object-Oriented Programming
             └── Classes & Objects
             └── Encapsulation
             └── Inheritance
             └── Polymorphism & Abstraction
             └── Interfaces & Enums

WEEK 9-12:  Intermediate Java
             └── Exception Handling
             └── Collections (List, Map, Set)
             └── Generics
             └── Java 8 (Lambda, Streams)
             └── File I/O

WEEK 13-16: Advanced Java
             └── Design Patterns (Singleton, Factory, POM)
             └── Multithreading
             └── Maven Project Management
             └── Git Version Control

WEEK 17-20: Automation Testing
             └── TestNG Framework
             └── Selenium WebDriver
             └── Locator Strategies
             └── Waits & Synchronization
             └── Element Interactions

WEEK 21-24: Advanced Automation
             └── Page Object Model Framework
             └── Data-Driven Testing
             └── Cross-Browser Testing
             └── API Testing (Rest Assured)
             └── Reporting (Extent Reports)
             └── CI/CD (Jenkins basics)
```

---

## 🎯 DAILY PRACTICE RECOMMENDATIONS

```
📌 First 2 months:
   - Solve 2-3 Java coding problems daily
   - Build small projects (calculator, student management)
   - Practice on: HackerRank, LeetCode (Easy problems)

📌 Months 3-4:
   - Write automation scripts daily
   - Automate real websites (practice sites):
     • https://www.saucedemo.com/
     • https://the-internet.herokuapp.com/
     • https://demoqa.com/
     • https://automationexercise.com/

📌 Months 5-6:
   - Build a complete framework from scratch
   - Contribute to open-source projects
   - Practice interview questions
   - Create a portfolio project on GitHub
```

---

> **💡 Final Tip:** The best way to learn is by DOING. Don't just read this guide - type out every example, modify it, break it, fix it, and experiment. Every error you encounter and solve makes you a better programmer and tester!

**Happy Learning! 🚀**
