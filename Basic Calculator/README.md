# Basic Calculator in C#

## Introduction
This is a simple console-based calculator built using C#. It allows users to perform basic arithmetic operations, including addition, subtraction, multiplication, and division.

## Features
- Accepts user input for two numbers.
- Allows selection of an arithmetic operation (`+`, `-`, `*`, `/`).
- Displays the result of the computation.
- Prevents division by zero errors.
- Provides error handling for invalid operations.

## How to Use
1. Run the program in a C# development environment (e.g., Visual Studio, Visual Studio Code).
2. Enter the first number when prompted.
3. Select an operation from `+`, `-`, `*`, or `/`.
4. Enter the second number.
5. View the result displayed on the console.

## Code Example
```csharp
using System;

Console.Write("Please Select A Number: ");
string userInput = Console.ReadLine();
double number = Convert.ToDouble(userInput);

Console.Write("Choose an operation (+, -, *, /): ");
char operation = Convert.ToChar(Console.ReadLine());

Console.Write("Choose a second number: ");
string userInput2 = Console.ReadLine();
double number2 = Convert.ToDouble(userInput2);

double result = 0;
if (operation == '+')
{
    result = number + number2;
}
else if (operation == '-')
{
    result = number - number2;
}
else if (operation == '*')
{
    result = number * number2;
}
else if (operation == '/')
{
    if (number2 != 0)
    {
        result = number / number2;
    }
    else
    {
        Console.WriteLine("Error: Division by zero is not allowed.");
        return;
    }
}
else
{
    Console.WriteLine("Invalid operation selected.");
    return;
}

Console.WriteLine($"The result is: {result}");
```

## Enhancements
- Improve input validation to prevent non-numeric entries.
- Add support for additional mathematical operations (e.g., modulus, exponentiation).
- Implement a loop to allow multiple calculations without restarting the program.

## License
This project is open-source and free to use for learning purposes.

---

Happy coding! 🚀
