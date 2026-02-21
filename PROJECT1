# Number-Guessing-Game
#An interactive game where users guess a random number.
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int secretNumber, userGuess, attempts = 0;

    // Seed the random number generator using the current time
    // This ensures a different random number is generated each time the program runs
    srand(time(NULL));

    // Generate a random number between 1 and 100
    // rand() % 100 gives a number in the range [0, 99]. Adding 1 shifts the range to [1, 100]
    secretNumber = (rand() % 100) + 1;

    printf("Welcome to the Number Guessing Game!\n");
    printf("I have chosen a number between 1 and 100. Try to guess it!\n");

    // Loop until the user guesses the correct number
    do {
        printf("\nEnter your guess: ");
        // Ensure input is an integer
        if (scanf("%d", &userGuess) != 1) {
            printf("Invalid input. Please enter an integer.\n");
            // Clear the input buffer to prevent an infinite loop with invalid input
            while (getchar() != '\n'); 
            continue;
        }
        
        attempts++; // Increment the number of attempts

        // Provide feedback on the guess
        if (userGuess < secretNumber) {
            printf("Too low! Try a higher number.\n");
        } else if (userGuess > secretNumber) {
            printf("Too high! Try a lower number.\n");
        } else {
            printf("\nCongratulations! You guessed the correct number (%d) in %d attempts.\n", secretNumber, attempts);
        }
    } while (userGuess != secretNumber); // Continue the loop as long as the guess is incorrect

    return 0;
}
