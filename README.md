# Rock-Paper-Scissor-Game
java language base rock paper scissor game by using random function of java 
<br>
import java.util.Scanner;
import java.util.Random;

public class Rock_paper_scissor {
    public static void main(String[] args) {
        int user, computer, rock, paper, scissor, rounds = 5;
        Scanner sc = new Scanner(System.in);
        Random random = new Random();
        rock = 0;
        paper = 1;
        scissor = 2;

        System.out.println("********ROCK_PAPER_SCISSOR_GAME********\n\n");

        for (int round = 1; round <= rounds; round++) {0
            System.out.println("Round " + round);
            System.out.print("ENTER YOUR CHOICE (rock=0; paper=1; scissor=2):- ");
            user = sc.nextInt();

            while (user > 2 || user < 0) {
                System.out.println("Inappropriate input. Please enter a number in the range 0 to 2.");
                user = sc.nextInt();
            }

            if (user == rock) {
                System.out.println("Your choice is ROCK");
            } else if (user == paper) {
                System.out.println("Your choice is PAPER");
            } else {
                System.out.println("Your choice is SCISSOR");
            }

            computer = random.nextInt(3);

            if (computer == rock) {
                System.out.println("Computer choice is ROCK");
            } else if (computer == paper) {
                System.out.println("Computer choice is PAPER");
            } else {
                System.out.println("Computer choice is SCISSOR");
            }

            while (user == computer) {
                System.out.println("DRAW! Try again.");
                user = sc.nextInt();

                while (user > 2 || user < 0) {
                    System.out.println("Inappropriate input. Please enter a number between 0 and 2:");
                    user = sc.nextInt();
                }

                computer = random.nextInt(3);

                if (user == rock) {
                    System.out.println("User chose ROCK");
                } else {
                    if (user == paper) {
                        System.out.println("User chose PAPER");
                    } else {
                        System.out.println("User chose SCISSORS");
                    }
                }

                if (computer == rock) {
                    System.out.println("Computer chose ROCK");
                } else {
                    if (computer == paper) {
                        System.out.println("Computer chose PAPER");
                    } else {
                        System.out.println("Computer chose SCISSORS");
                    }
                }
            } // END DRAW

            if (computer == rock) {
                if (user == paper) {
                    System.out.println("********:YOU WON:********");
                } else {
                    System.out.println("********:COMPUTER WON:********");
                }
            } else if (computer == paper) {
                if (user == scissor) {
                    System.out.println("********:YOU WON:********");
                } else {
                    System.out.println("********:COMPUTER WON:********");
                }
            } else if (computer == scissor) {
                System.out.println("********:YOU WON:********");
            } else {
                System.out.println("********:COMPUTER WON:********");
            }
        } // End of rounds loop
    }
}

