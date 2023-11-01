#include <iostream>
#include <string>
#include <ctime>
#include <cstdlib>

void start_game() {
    int user_score = 0;
    int computer_score = 0;
    char user_input;
    srand(time(0));

   while (user_score < 10 && computer_score < 10) {
       std::cout << "Enter your move: ";
       std::cin >> user_input;

       int computer_move = rand() % 3 + 1;

       if (user_input == '1' || user_input == '2') {
           if (computer_move == 1) {
               std::cout << "Computer moves 1. It's a 2 point shot!" << std::endl;
               computer_score += 2;
           } else if (computer_move == 2) {
               std::cout << "Computer moves 2. It's a 3 point shot!" << std::endl;
               computer_score += 3;
        } else {
            std::cout << "Computer moves 3. It's a free throw!" << std::endl;
            computer_score += 1;
        }
    } else if (user_input == '3') {
        std::cout << "You take a 3 point shot. Good job!" << std::endl;
        user_score += 3;
    } else {
        std::cout << "Invalid input. Try again." << std::endl;
        continue;
    }

    std::cout << "Your score: " << user_score << ", Computer score: " << computer_score << std::endl;
 }

 if (user_score == 10) {
     std::cout << "Congratulations! You win!" << std::endl;
 } else {
     std::cout << "Computer wins! Better luck next time." << std::endl;
 }
}

int main() {
    std::string player_name;
    std::cout 
