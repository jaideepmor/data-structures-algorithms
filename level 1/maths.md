# ***** basics of program. and maths -->  
                        snytax - 
                        1.how to print,variables,operators ->
				                   loops,inc.operator

                        2.how to take input - integer -> Scanner scn = new Scanner(System.in);
                                         			          int t = scn.nextInt();

                                           - string -> Scanner scn = new Scanner(System.in);  
                                        			         String name = scn.nextLine();

			                                      - for integer and string both ->Scanner scn = new Scanner(System.in); 
                                 	                  			                  int n = Integer.parseInt(scn.nextLine());

  optional problem
  # 1.grading system - 
  import java.util.*;

public class Main {

  public static void main(String[] args) {
    Scanner scn = new Scanner(System.in);
    int marks = scn.nextInt();
    // Write your code here
    if (marks > 90)
    {
      System.out.println("excellent");
    }  
    else if( 90 >= marks && marks >80 )
    {
      System.out.println("good");
    }
    else if( 80 >= marks && marks >70 )
    {
      System.out.println("fair");
    }
    else if( 70 >= marks && marks >60 )
    {
      System.out.println("meets expectations");
    }
    else if(marks <= 60)
    {
      System.out.println("below par");
    }

      }
}                   
# question no. -->
# 1.is a no. prime - 

# 2.print all primes till n -

# 3.print fibonacci no. till n - 

# 4.count digits in a number -

# 5.digit of a number -

# 6.reverse a no. -

# 7.inverse of a no. -

# 8.rotate a no. -

# 9.GCD and LCM -

# 10.prime factorisation of a no. -

# 11.pythagorean triplet -

# 12.the curious case of benjamin bulbs -

  
# extra points and tips --> 
