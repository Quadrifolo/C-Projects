\# Number Guessing Game

Welcome to the \*\*Number Guessing Game\*\*! This is a simple
console-based game written in C# where the player guesses a randomly
generated number between 1 and 100. The game provides hints like \"Too
high\" or \"Too low\" until the player guesses the correct number.

\-\--

\## \*\*Features\*\* - Generates a random number between 1 and 100. -
Provides feedback on each guess (too high, too low, or correct). -
Tracks the number of attempts taken to guess the number. - Option to
play again after guessing the correct number.

\-\--

\## \*\*How to Play\*\* 1. Clone or download the repository to your
local machine. 2. Open the project in your preferred IDE (e.g., Visual
Studio, Visual Studio Code). 3. Run the program. 4. Follow the on-screen
instructions to guess the number. 5. Enjoy the game!

\-\--

\## \*\*Code Overview\*\* The game is implemented in C# and consists of
the following key components: 1. \*\*Random Number Generation\*\*: A
random number between 1 and 100 is generated using the \`Random\` class.
2. \*\*User Input Handling\*\*: The program reads the player\'s guess
and validates it. 3. \*\*Game Logic\*\*: The program checks if the guess
is correct, too high, or too low and provides feedback. 4. \*\*Play
Again Option\*\*: After guessing the correct number, the player can
choose to play again or exit.

\-\--

\## \*\*Code Example\*\* Here's a snippet of the main game logic:

\`\`\`csharp Random random = new Random(); int secretNumber =
random.Next(1, 101); int guess = 0; int attempts = 0; bool
hasGuessedCorrectly = false;

Console.WriteLine(\"Welcome to the Number Guessing Game!\");
Console.WriteLine(\"I\'m thinking of a number between 1 and 100. Can you
guess it?\");

while (!hasGuessedCorrectly) { Console.Write(\"Enter your guess: \");
string input = Console.ReadLine();

if (int.TryParse(input, out guess)) { attempts++;

if (guess == secretNumber) { hasGuessedCorrectly = true;
Console.WriteLine(\$\"Congratulations! You guessed the number in
{attempts} attempts.\"); } else if (guess \< secretNumber) {
Console.WriteLine(\"Too low! Try again.\"); } else {
Console.WriteLine(\"Too high! Try again.\"); } } else {
Console.WriteLine(\"Invalid input. Please enter a valid number.\"); } }
