#include <iostream>
#include <cstdlib>
#include <ctime>

void guessTheNumber() {
    // Number guessing game
    
    // Initialize random seed
    std::srand(std::time(nullptr));
    
    // Generate random number between 1 and 100
    int numberToGuess = std::rand() % 100 + 1;
    int guess = 0;
    
    std::cout << "Welcome to 'Guess the Number'!" << std::endl;
    std::cout << "I have chosen a number between 1 and 100. Can you guess it?" << std::endl;
    
    while (guess != numberToGuess) {
        std::cout << "Enter your guess: ";
        std::cin >> guess;
        
        if (guess < numberToGuess) {
            std::cout << "Too low! Try again." << std::endl;
        } else if (guess > numberToGuess) {
            std::cout << "Too high! Try again." << std::endl;
        } else {
            std::cout << "Congratulations! You guessed the correct number." << std::endl;
        }
    }
}

int main() {
    guessTheNumber();
    return 0;
}
