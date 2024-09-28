# C-programming-by-CoderxRaghav
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    srand(time(0));  
    // GENERATING A RANDOM NUMBER//
    int randomNumber = (rand() % 100) + 1;  
    int numberofGuess = 0;
    int guessednumber;
    // TAKING USER INPUT //
    do {
        printf("Guess the number: ");
        scanf("%d", &guessednumber);  
        
        if (guessednumber > randomNumber) {
            printf("Lower number please\n");
        } 
        else if (guessednumber < randomNumber) {
            printf("Higher number please\n");
        }
        numberofGuess++;
        
    } while (guessednumber != randomNumber);
    
    printf("You guessed the number correct in %d guesses\n", numberofGuess);
    return 0;
}
