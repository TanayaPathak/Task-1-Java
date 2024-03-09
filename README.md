# Task-1-Java
import java.util.Random; 

import java.util.Scanner; 

  

public class GuessTheNumberGame { 

    public static void main(String[] args) { 

        System.out.println("Welcome to Guess the Number Game!"); 

        Scanner scanner = new Scanner(System.in); 

        Random random = new Random(); 

        String playAgain = "yes"; 

        int totalRounds = 0; 

        int totalAttempts = 0; 

        while (playAgain.toLowerCase().equals("yes")) { 

            totalRounds++; 

            int attempts = 0; 

            int numberToGuess = random.nextInt(100) + 1; 

            System.out.println("I have selected a number between 1 and 100. Try to guess it!"); 

            while (true) { 

                System.out.print("Enter your guess: "); 

                int guess = scanner.nextInt(); 

                attempts++; 

                if (guess < numberToGuess) { 

                    System.out.println("Too low! Try again."); 

                } else if (guess > numberToGuess) { 

                    System.out.println("Too high! Try again."); 

                } else { 

                    System.out.println("Congratulations! You've guessed the number " + numberToGuess + " correctly in " + attempts + " attempts!"); 

                    totalAttempts += attempts; 

                    break; 

                } 

            } 

            System.out.print("Do you want to play again? (yes/no): "); 

            playAgain = scanner.next(); 

        } 

        System.out.println("Game Over! You played " + totalRounds + " round(s) and took " + totalAttempts + " attempt(s) in total."); 

    } 

} 

  

 

 
