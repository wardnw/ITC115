//Nate Ward 1/11/205 ITC115
//program to get a random number and check it against user input

package pkg.nward.guessnumber;

import java.util.Random;
import java.util.Scanner;

public class Program {
	
	static Scanner scan = new Scanner(System.in);
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Program.selectOption();

	}

	
	
	//get user guesses 
	private static int getInput(){
		System.out.println("Enter your guess:");
		int input = scan.nextInt();
		return input;
	}
	
	//menu
	private static void selectOption(){
		System.out.println("Select an option:");
		System.out.println("1: New game");
		System.out.println("2: Exit");
		
		int input = scan.nextInt();
		
		switch (input){
		case 1: validateGuess(getMagicNumber());
		break;
		case 2: System.exit(0);
		break;
		default: System.out.println("Enter a valid option.");
		selectOption();
		break;
		}
		
		
		
	}
	
	//check user's guess against the magic number
	private static void validateGuess(int m){
		int userGuess = getInput();
		//int counter = 0;
		int scoreCounter = 10;
		
		for(int i = 0; i < 10; i++){
			if(userGuess == m){
				System.out.println("Correct.");
				System.out.println("Your score is " + scoreCounter);
				break;
			}
			else if(userGuess < m){
				System.out.println("Too low.");
				//counter++;
				System.out.println("You have " + (9 - i) + " attempts remaining.");
				userGuess = getInput();
				scoreCounter--;
				
			}
			else if(userGuess > m){
				System.out.println("Too high.");
				//counter++;
				System.out.println("You have " + (9 - i) + " attempts remaining.");
				userGuess = getInput();
				scoreCounter--;
				
			}
			else{
				System.out.println("Invalid input.");
				userGuess = getInput();
				System.out.println("You have " + (9 - i) + " attempts remaining.");
				scoreCounter--;
			
				
			
			}
			while(i == 9){
				System.out.println("No attempts remaining, returning to main menu");
				break;
			}
		}
			selectOption();
	}
	
	//get the number to guess
	private static int getMagicNumber(){
		int m = getRandInt(1, 500);
		return m;
	}
	
	//return a random integer btw 1 and 500
	private static int getRandInt(int min, int max){
		Random rand = new Random();
		int r = rand.nextInt((max - min) + 1);
		return r;
	}

}
