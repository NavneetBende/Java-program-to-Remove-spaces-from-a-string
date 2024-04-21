Remove spaces from String
In this page we will look at how to write a java program to remove spaces from a string. 

Here we will store the string in a character array lets say s and that original string will contain the spaces in between.

Example:- 

Input string: “Prep  insta”
Output string: “Prepinsta”
Java program to Remove spaces from a string
Algorithm
Take string input from user and store it in the variable called “s”.
After that convert that string to char array using toCharArray() method.
Make a string buffer object and run the for loop start from i=0 to i<c.length.
check if( (c[i] != ‘ ‘) && (c[i]!= ‘\t’ )) append that character to string buffer and after that simply print string buffer.
Code in Java (Method-1 without using in-built method)
Run
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
	  Scanner sc =new Scanner(System.in);
	  String s = "Prepinsta is best";
	  char[] c = s.toCharArray();
	  StringBuffer sb = new StringBuffer();
	  
	  
	  for (int i = 0; i < c.length; i++) {
	     if( (c[i] != ' ') && (c[i]!= '\t' )) {
	    	 sb.append(c[i]);
	     }    	
          }
	  System.out.println("String after removing spaces : "+sb);
    }
}
Output
String after removing spaces : Prepinstaisbest
Note
Make a StringBuffer object and check each for each character array that element should not be blank there should not be any whitespaces if the condition is true append that element to StringBuffer object after that print StringBuffer object in which String doesn't contain any blank spaces.
Code in Java (Method-2 using in-built method)
Run
import java.util.Scanner;

public class Main {
      public static void main(String[] args) {
      StringBuffer sb = new StringBuffer();
	String s = "Prepinsta is best";
	String[] s1 = s.split("[\\s]");
	for (String string : s1) {
		sb.append(string);
	}
    System.out.println(sb);
   }
}
Output
String after removing spaces : Prepinstaisbest
