# Tax Calculator App

A simple command-line Java application that calculates annual income tax for a list of people using fixed tax slabs.

This repository contains a minimal, easy-to-understand example suitable for beginners learning Java, console I/O, arrays, and simple conditional logic.

## Features

- Read number of people from console
- For each person, read name and annual income
- Calculate tax using simple slabs (see "Tax Rules")
- Print each person's name and tax amount (₹ symbol used)

## Tax Rules Used

- Income >= 300,000 : 20% tax
- Income >= 100,000 and < 300,000 : 10% tax
- Income < 100,000 : 0% tax

Note: These are example slabs for this app only and not intended as real tax logic for any jurisdiction.

## Requirements

- Java Development Kit (JDK) 8 or newer
- A terminal/command prompt

## Project Structure

- src/main/java/com/internshala/javaapp/Main.java — main application

## How to Build and Run

1. Save the Java source file under the package path:

   src/main/java/com/internshala/javaapp/Main.java

2. Compile from the project's root directory:

```bash
javac -d out src/main/java/com/internshala/javaapp/Main.java
```

3. Run the application:

```bash
java -cp out com.internshala.javaapp.Main
```

Alternatively, from the package directory you can compile and run directly (adjust paths as needed):

```bash
cd src/main/java
javac com/internshala/javaapp/Main.java
java com.internshala.javaapp.Main
```

## Example Session

```
 Tax Calculator App 
----- WELCOME ------

Enter total person count: 
3

Enter name 1 : 
Asha
Enter Asha's Annual Income: 
250000

Enter name 2 : 
Ravi
Enter Ravi's Annual Income: 
85000

Enter name 3 : 
Meera
Enter Meera's Annual Income: 
420000

 Names with liable taxes
---------------------------
 Asha : ₹ 25000
 Ravi : ₹ 0
 Meera : ₹ 84000
```

(The rupee symbol is printed using Unicode '\u20B9' in the program.)

## Code Explanation (brief)

- The app reads the number of people, then loops to collect each person's name and income into arrays.
- For each person, it calls calculateTax(name, income) which applies the slab logic and prints the tax with the rupee symbol.
- The tax calculation uses integer math (long). For more precision (e.g., decimals), consider using BigDecimal.

## Possible Improvements

- Validate inputs (non-negative incomes, non-empty names)
- Support decimal incomes and more realistic tax brackets
- Output formatted currency with grouping separators
- Add unit tests
- Move logic into separate classes for better testability

## Contributing

Feel free to open pull requests or suggest improvements. For small fixes, create a branch, add tests (if appropriate), and submit a PR.

## License

This project is provided under the MIT License. See LICENSE file for details (or add one if needed).
