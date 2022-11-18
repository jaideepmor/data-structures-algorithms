# ***** Pattern --> 
                         important note - 
                         - loop 1 - represents - 
						 - loop 2              - 
						 - loop 3              - 

# questions -->
# 1.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        
        for(int i=1;i<=n;i++)
        {    
            for(int j=1;j<=i;j++)
            {
            System.out.print("*\t");
            }
            System.out.println(); 
               
            
               
        }

    }
}
# 2.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);

        int n = scn.nextInt();
        int m = n;
        for(int i=1;i<=n;i++)
         
         { 
             for(int j=m;j>=1;j--)
             {
                 
                 System.out.print("*\t");
             } 
             m--;
         
             System.out.println();
         }


    }
}
# 3.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        

        for(int i=1;i<=n;i++) {
            for(int j=1;j<=n-i;j++) {  
                System.out.print("\t");
            }
            for(int k=1;k<=i;k++) {
                System.out.print("*\t");
                
            }
            System.out.println();
        }

    }
}
# 4.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);

        int n = scn.nextInt();
        int m=n;
        for(int i=1;i<=n;i++)
        {
            for(int j=1;j<i;j++)
            {
                System.out.print("\t");
            }
            for(int k=1;k<=m;k++)
            {
                System.out.print("*\t");
            }m--;
            System.out.println();
        }

    }
}
# 5.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int sp = n/2;
        int st = 1;
        for (int i=1;i<=n;i++)
        {
            for(int j=1;j<=sp;j++)
            {
              System.out.print("\t");  
            }
            
            
            for(int k=1;k<=st;k++)
            {
               System.out.print("*\t");         
            }
            if(i<=n/2)
            { sp--;
              st+=2;
        
            }
            else
            { sp++;
              st-=2;

            }
            System.out.println();
        }

    }
}
# 6.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int star = n/2+1;
        int space = 1;
        // write ur code here
         for(int i=1; i<=n; i++){
        for(int j=1; j<=star; j++){
           System.out.print("*\t");
           } 
         for(int j=1; j<=space; j++){
            System.out.print("\t"); 
         } 
          for(int j=1; j<=star; j++){
              System.out.print("*\t");  
          }
          if(i<=n/2){
              star--;
              space+=2;
          }
          else{
              star++;
              space-=2;
          }
            System.out.println();
         }
    }
}
# 7.
import java.util.*;

public class Main {
  public static void main(String[] args)
  {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    for (int i = 1; i <= n; i++) //decides the number of rows for output printing
    {
      for (int j = 1; j <= n; j++) //prints the stars in the row
      {
        System.out.print("*");
    }
      System.out.println();   //changes the row on output console
    }
  }
}
# 8.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();

        int nsp = n - 1;

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < nsp; j++) {
                System.out.print("\t");
            }

             System.out.print("*\t");

            nsp--;
            System.out.println();
        }

    }
}
# 9.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        // 
        for(int i=1; i<=n;i++){
            for(int j=1; j<=n; j++){
                if (i==j){
                    System.out.print("*\t");
                }
                else if(i+j==n+1){
                    System.out.print("*\t");
                }
                else{
                    System.out.print("\t");
                }
               

            }System.out.println();
        }

    }
}
# 10.
import java.util.*;

public class Main{

public static void main(String[] args) {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int os = n/2;
    int is = -1;
     // write ur code here
        for(int i=1; i<=n; i++) {
            for(int j=1; j<=os ; j++) {
                System.out.print("\t");
            }

            System.out.print("*\t");

            for(int j=1; j<=is ; j++) {
                System.out.print("\t");
            }
            
            if(i > 1 && i < n) {
                System.out.print("*\t");
            }

            if(i <= n/2){
                os--; is+=2;
            } else {
                os++; is-=2;
            }      
             
            System.out.println();
        }

}
}
# 11.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in); 


        int n =  scn.nextInt();
        int val = 1;
        for(int i=1; i<=n; i++){
            for(int j=1; j<=i; j++){
              System.out.print(val + "\t"); 
              val++;                                                                     
            }
            System.out.println();
        }
    }
}
# 12.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int a = 0;
        int b = 1;
        // write ur code here
     
       for(int i=1; i<=n; i++){
           for(int j=1; j<=i; j++){
                 int c = a+b ;    
             System.out.print(a + "\t");
             a=b;
             b=c;
           }
           System.out.println();
       } 
    }
}
# 13.
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        for(int i=0; i<n; i++){
            int icj = 1;
            for(int j=0; j<=i; j++){
                System.out.print(icj+"\t");
                int icjp1 = icj * (i - j)/ (j+1);
                icj = icjp1;
            }
            System.out.println();
        }

        

    }
}
# 14.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);
        int x = scn.nextInt();
        for(int i=1; i<=10; i++){
              int v = x*i;
        System.out.println(x + " * " + i + " = " + v);
        }
        
    }
}
# 15.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int sp = n/2;
        int st = 1;
        int val = 1;
         for(int i=1; i<=n; i++){
             for(int j=1; j<=sp; j++){
                 System.out.print("\t");
             }
             int cval = val;
             for(int j=1; j<=st; j++){
                 System.out.print(cval+"\t");
                 if(j<=st/2){
                   cval++;
                 }
                 else{
                   cval--;
                 }
                 
             }
               if(i<=n/2)
                 {
                    sp--;
                    st+=2;
                    val++;
                 }
                 else
                 {
                    sp++;
                    st-=2; 
                    val--;
                 }

               System.out.println();
         }

    }
}
# 16.
import java.util.*;

public class Main{

public static void main(String[] args) {
    Scanner scn = new Scanner(System.in);
     int n = scn.nextInt();
     int sp = 2*n-3;
     int st = 1;

    for(int i=1; i<=n; i++){
        int val = 1;

        for(int j=1; j<=st; j++){
            System.out.print(val+"\t");
            val++;
        }

        for(int j=1; j<=sp; j++){
            System.out.print("\t");
        }

        if(i==n){
            st--;
            val--;
        }

        for(int j=1; j<=st; j++){
            val--;
            System.out.print(val+"\t");
        }

        st++; sp-=2;
        System.out.println(); 
        
    }
 }
}
# 17.
import java.util.*;

public class Main {
  public static void main(String[] args)
  {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int sp = n / 2; //variable to store space count
    int st = 1;     //variable to store star count
    for (int i = 1; i <= n; i++)
    {
      for (int j = 1; j <= sp ; j++) //printing whitespaces
      {
        if ( i == n / 2 + 1)    //checking middle row
        {
          System.out.print("*	");
        }
        else
        {
          System.out.print("	");
        }
      }
      for (int j = 1 ; j <= st; j++) // printing the stars
      {
        System.out.print("*	");
      }
      if ( i <= n / 2)    //checking if less than or equal to middle row
      {
        st++;       //increasing stars till middle row
      }
      else {
        st--;       //decreasing stars post middle row
      }
      System.out.println(); //Changing the row
    }
  }
}
# 18.
import java.util.*;

public class Main{

public static void main(String[] args) {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int sp = 0;
    int st = n;
        for(int i=1; i<=n; i++){
             for(int j=1; j<=sp;j++){
                 System.out.print("\t");
                 }
             for(int j=1; j<=st; j++){
                 if(i>1 && i<=n/2 && j>1 && j<st){
                 System.out.print("\t");
                 }
                 else{
                 System.out.print("*\t");
                 }
                 }
            
                 if(i<=n/2){
                     st-=2;
                     sp++;
                 }
                 else{
                     st+=2;
                     sp--;
                 }    
            System.out.println();     
    }

 }
}
# 19.
import java.util.*;

public class Main{

public static void main(String[] args) {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    
           for(int i=1; i<=n; i++){
               for(int j =1; j<=n; j++){
                   if(i==1){
                       if(j==n||j<=n/2+1){System.out.print("*\t");}
                       else{System.out.print("\t");}
                       }
                   else if(i<=n/2){
                       if(j==n||j==n/2+1){System.out.print("*\t");}
                       else{System.out.print("\t");}
                                  }
                else if(i==n/2+1){
                       System.out.print("*\t");
                       }
                   else if(i<n){
                         if(j==1||j==n/2+1){System.out.print("*\t");}
                       else{System.out.print("\t");}
                            }
                   else{
                          if(j==1||j>=n/2+1){System.out.print("*\t");}
                       else{System.out.print("\t");}
                       }

            
               }
            System.out.println();
           }

 }
}
# 20.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
                if (j == 1 || j == n) {
                    System.out.print("*\t");
                } else if (i > n / 2 && (i == j || i + j == n + 1)) {
                    System.out.print("*\t");
                } else {
                    System.out.print("\t");
                }
            }

            System.out.println();
        }
    }
}
# optional -
# 21.

# 22.
import java.util.*;

public class Main{

public static void main(String[] args) {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    
    int nst = n;
    int nsp = 0;
    for(int i = 0; i < n; i++){
        for(int j = 0; j < nsp; j++){
            System.out.print("\t");
        }

        for(int j = 0; j < nst; j++){
            System.out.print("*\t");
        }

        if(i < n / 2){
            nst -= 2;
            nsp++;
        } else {
            nst += 2;
            nsp--;
        }

        System.out.println();
    }

 }
}

# extra points and tips --> 