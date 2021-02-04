/*
 * Class: CMSC203 
 * Title: Lab 1 - Driver and Data Element Driver to test a class
 * Instructor: Khandan Monshi
 * Description: Created a driver class to ask user to input name, rating and 
 * sold tickets of a movie while using the Movie class
 * Due: 2/4/2021
 * Platform/compiler: Eclipse
 * I pledge that I have completed the programming assignment independently.
   I have not copied the code from a student or any source.
   I have not given my code to any student.
   Print your Name here: Bianelis Liriano
*/


import java.util.Scanner;

public class MovieDriver {

	public static void main(String[] args) {
		
		Scanner in = new Scanner(System.in);  //to get user input
		Movie m = new Movie();   //object to use Movie class
		
		
		String name; 		//user input movie name
		String mrating;		//user input movie rating
		int tickets;		//user input tickets sold
		char repeat;		//user input another movie validation
		
		
		do {
			
		System.out.println("Enter the name of a movie");
		name = in.nextLine();
		m.setTitle(name);        //sets the title of the movie to user input
		
		System.out.println("Enter the rating of the movie");
		mrating = in.nextLine();
		m.setRating(mrating);    //sets the rating of the movie to user input
		
		System.out.println("Enter the number of tickets sold for this movie");
		tickets = in.nextInt();
		in.nextLine();          //sets the number of tickets sold to user input
		
		m.setSoldTickets(tickets);  //calls toString from Movie class
		
		System.out.println(m.toString());  //prints toString from Movie class
		
		System.out.println("Do you want to enter another? ( y or n)");
		repeat = in.next().charAt(0);      //gets user letter input
		in.nextLine(); 	     //to read and discard the previous \n 
		
		} while ( repeat == 'y' || repeat == 'Y'); 
		
		System.out.println("Goodbye");

	}

}

