# Number Guessing Game in C#

## Introduction
This is a simple console-based Number Guessing Game implemented in C#. The program generates a random number between 1 and 100, and the player has to guess it based on hints provided by the game.

## Features
- Generates a random number between 1 and 100.
- Accepts user input for guessing the number.
- Provides feedback if the guess is too high, too low, or correct.
- Tracks the number of attempts.
- Handles invalid input gracefully.

## How to Play
1. Run the program in a C# development environment (e.g., Visual Studio, Visual Studio Code).
2. Enter a number between 1 and 100 when prompted.
3. The program will indicate whether your guess is too high, too low, or correct.
4. Continue guessing until you find the correct number.

## Code Example
```csharp
using System;

// Generates a random number between 1 and 100
Random num = new Random();
int rand1 = num.Next(1, 101);

int guess = 0;
int attempts = 0;
bool hasGuessedCorrectly = false;

Console.Write("Enter a number between 1 and 100: ");

while (!hasGuessedCorrectly)
{
    string userInput = Console.ReadLine();

    if (int.TryParse(userInput, out guess))
    {
        attempts++;

        if (guess == rand1)
        {
            hasGuessedCorrectly = true;
            Console.WriteLine($"You have guessed correctly in {attempts} attempts!");
        }
        else if (guess < rand1)
        {
            Console.WriteLine("Entry is too low, please try again.");
        }
        else
        {
            Console.WriteLine("Entry is too high, please try again.");
        }
    }
    else
    {
        Console.WriteLine("Invalid input. Please enter a valid number.");
    }
}
```

## Enhancements
- Add a limit to the number of attempts.
- Allow the player to restart the game without rerunning the program.
- Implement a scoring system based on the number of attempts.

## License
This project is open-source and free to use for learning purposes.

---

Happy coding! 🚀
