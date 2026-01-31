#include <iostream>
#include <cstdlib>
#include <vector>
#include <string>
#include <ctime>

std::string gameLogic(std::string player, std::string bot) {
    if (player == "rock") {
        if (bot == "rock") {
            return "tie";
        } else if (bot == "paper") {
            return "lose";
        } else {
            return "win";
        } 
    } else if (player == "paper") {
        if (bot == "rock") {
            return "win";
        } else if (bot == "paper") {
            return "tie";
        } else {
            return "lose";
        } 
    } else {
        if (bot == "rock") {
            return "lose";
        } else if (bot == "paper") {
            return "win";
        } else {
            return "tie";
        } 
    }
}

int main() {
    srand(time(nullptr));
    std::vector<std::string> item = {"rock", "paper", "scissor"};
    int playerScore = 0;
    int botScore = 0;
    std::string playerThrow;
    while(playerScore != 5 && botScore != 5) {
        std::cout << "Please make a choice between rock, paper or scissor!" << std::endl;
        std::cin >> playerThrow;
        if(playerThrow != "rock" && playerThrow != "paper" && playerThrow != "scissor")
        {
            std::cout << "Invalid Option. Please try again :)." << std::endl;
            continue;
        }
        std::string botThrow = item[rand() % 3];
        std::string result = gameLogic(playerThrow, botThrow);
        std::cout << "You chose " << playerThrow << " and the computer chose " << botThrow << std::endl;
        std::cout << "You " << result << "!" << std::endl;
        if(result == "win") {
            playerScore++;
        }
        if(result == "lose") {
            botScore++;
        }
        std::cout << "Score: " << playerScore << " - " << botScore << std::endl;
    }
    
    if (playerScore == 5) {
        std::cout << "CONGRATULATIONS YOU WIN!!!!";
    } else {
        std::cout << "GAME OVER";
    }
    
    return 0;
}




