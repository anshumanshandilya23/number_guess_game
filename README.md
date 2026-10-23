# number_guess_game
In this game the program generates the random number from 1 to 100 and the user has to guess the input number
here I am attaching the code of the game


// Number guess game.
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main()
{
    srand(time(NULL)); // intitialization for random number generator

    int randomnumber = rand() % 100 + 1; // generate random number between 1 to 100
    int no_of_guesses = 0;
    int guessed_number;
    do
    {
        printf("Guess the number : \n");
        scanf("%d", &guessed_number);
        if (guessed_number > randomnumber)
        {
            printf("Lower the value please\n");
        }
        else if (guessed_number < randomnumber)
        {
            printf("Higher the value please \n");
        }
        else
        {
            printf("conrgatulationsss!!! \n");
        }
        no_of_guesses++;
    } while (guessed_number != randomnumber);
    printf(" you guesses the number in %d guesses : \n", no_of_guesses);
    return 0;
}
