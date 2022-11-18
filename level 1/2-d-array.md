# ***** 2-D Array -->  i & j - n & m - rows & column - arr.length & arr.length[i]
 Scanner scn = new Scanner(System.in);
     int n = scn.nextInt();
     int m = scn.nextInt();
     int[][] arr = new int[n][m];
     for(int i=0; i<n; i++)
     {
       for(int j=0; j<m; j++)
       {
         arr[i][j] = scn.nextInt();
       }
     }
     for(int i=0; i<arr.length; i++)
     {
       for(int j=0; j<arr[i].length; j++)
       {
          System.out.print(arr[i][j]+" ");
       }
       System.out.println();
     }

# questions -->
# 1.matrix multiplication - 
import java.io.*;
import java.util.*;

public class Main{

public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int r1 = scn.nextInt();
    int c1 = scn.nextInt();
    int[][] m1 = new int[r1][c1];
    for(int i=0; i<m1.length; i++)
    {
        for(int j=0; j<m1[i].length; j++)
        {
          m1[i][j] = scn.nextInt();  
        }
    }
    int r2 = scn.nextInt();
    int c2 = scn.nextInt();
    int[][] m2 = new int[r2][c2];
    for(int i=0; i<m2.length; i++)
    {
        for(int j=0; j<m2[i].length; j++)
        {
          m2[i][j] = scn.nextInt();  
        }
    }
    if(c1!=r2)
    {
     System.out.print("Invalid input");
     return;   
    }
    int[][] prd = new int[r1][c2];
    for(int i=0; i<prd.length; i++)
    {
        for(int j=0; j<prd[i].length; j++)
        {
            for(int k=0; k<c1; k++)
            {
              prd[i][j] += m1[i][k]*m2[k][j];  
            }
        }
    }
     for(int i=0; i<prd.length; i++)
    {
        for(int j=0; j<prd[i].length; j++)
        {
        System.out.print(prd[i][j]+" ");    
        }
        System.out.println();
    }
 }

}
# 2.the state of wakanda 1 - wave traversal -
import java.io.*;
import java.util.*;

public class Main{

public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int r = scn.nextInt();
    int c = scn.nextInt();
    int[][] m = new int[r][c];
    for(int i=0; i<m.length; i++)
    {
        for(int j=0; j<m[i].length; j++)
        {
          m[i][j] = scn.nextInt();
        }
    }
    for(int j=0; j<m[0].length; j++)
     { if(j%2==0)
       {
          for(int i=0; i<m.length; i++) 
              {
                 System.out.println(m[i][j]);
              }  
       }else
       {
          for(int i=m.length-1; i>=0; i--)
          {
              System.out.println(m[i][j]);
          }
       }

     }
 }

}
# 3.spiral display/matrix -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
      Scanner scn = new Scanner(System.in);
      int r = scn.nextInt();
      int c = scn.nextInt();
      int[][] m = new int[r][c];
      for(int i=0; i<m.length; i++)
      { for(int j=0; j<m[0].length; j++)
         {
          m[i][j] = scn.nextInt(); 
         }
      }
      int rmin=0;
      int cmin=0;
      int rmax=m.length-1;
      int cmax=m[0].length-1;
      int count=0;
      int t = r*c;
      while(count<t)
      {
          for(int i=rmin,j=cmin; i<=rmax&&count<t; i++)
          {
           System.out.println(m[i][j]);
           count++;
          }cmin++;
           
           for(int i=rmax,j=cmin; j<=cmax&&count<t; j++)
          {
          System.out.println(m[i][j]);
          count++;
          }rmax--;
          
           for(int i=rmax,j=cmax; i>=rmin&&count<t; i--)
          {
          System.out.println(m[i][j]);
          count++;
          }cmax--;

           for(int i=rmin,j=cmax; j>=cmin&&count<t; j--)
          {
          System.out.println(m[i][j]);
          count++;
          }rmin++;

      }
    }

}
# 4.exit point of matrix -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int m = scn.nextInt();
        int[][] arr = new int[n][m];
        for(int i=0; i<arr.length; i++)
        {
            for(int j=0; j<arr[0].length; j++)
            {
                arr[i][j] = scn.nextInt();
            }
        }
        int dir = 0;
        int i = 0;
        int j = 0;
        while(true)
        {  dir = (dir + arr[i][j])%4;
           if(dir==0)
           {j++;}
           else if(dir==1)
           {i++;} 
           else if(dir==2)
           {j--;}
           else if(dir==3)
           {i--;}
           if(i<0)
           {i++;break;}
           else if(j<0)
           {j++;break;}
           else if(i==arr.length)
           {i--;break;}
           else if(j==arr[0].length)
           {j--;break;}
        }
        System.out.println(i);
        System.out.println(j);

    }

}
# 5.rotate by 90 degree -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int[][] arr = new int[n][n]; 

        for(int i=0; i<arr.length; i++) {
            for(int j=0; j<arr[0].length; j++) {
                arr[i][j] = scn.nextInt();
            }
        }

        for(int i=0; i<arr.length; i++) {
            for(int j=i; j<arr[0].length; j++) {   
                int temp = arr[i][j];
                arr[i][j] = arr[j][i];
                arr[j][i] = temp;            
            }
        }

        for(int i=0; i<arr.length; i++) {
            int l=0;
            int r=arr.length-1;
            while(l<r) {
              int temp = arr[i][l];
              arr[i][l] = arr[i][r];
              arr[i][r] = temp;
              l++;
              r--;  
            }
        }
        display(arr);
    }

    public static void display(int[][] arr) {
        for(int i = 0; i < arr.length; i++) {
            for(int j = 0; j < arr[0].length; j++) {
                System.out.print(arr[i][j] + " ");
            }
            System.out.println();
        }
    }

}
# 6.ring rotate - 
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int m = scn.nextInt();

    int[][] arr = new int[n][m];
    for (int i = 0; i < n; i++) {
      for (int j = 0; j < m; j++) {
        arr[i][j] = scn.nextInt();
      }
    }

    int s = scn.nextInt();
    int r = scn.nextInt();

    rotateShell(arr, s, r);
    display(arr);
  }

  public static void rotateShell(int[][] arr, int s, int r) {
    int[] oned = fillOnedFromShell(arr, s);
    rotate(oned, r);
    fillShellFromOned(arr, s, oned);
  }

  public static void rotate(int[] oned, int r) {
    r = r % oned.length;
    if (r < 0) {
      r += oned.length;
    }

    reverse(oned, 0, oned.length - r - 1);
    reverse(oned, oned.length - r, oned.length - 1);
    reverse(oned, 0, oned.length - 1);
  }

  public static void reverse(int[] arr, int i, int j) {
    while (i < j) {
      int temp = arr[i];
      arr[i] = arr[j];
      arr[j] = temp;
      i++;
      j--;
    }
  }

  public static int[] fillOnedFromShell(int[][] arr, int s) {
    int minr = s - 1;
    int minc = s - 1;
    int maxr = arr.length - s;
    int maxc = arr[0].length - s;
    int size = 2 * (maxr - minr) + 2 * (maxc - minc);
    int[] oned = new int[size];

    int index = 0;
    for (int i = minr, j = minc; i <= maxr; i++) {
      oned[index] = arr[i][j];
      index++;
    }

    for (int i = maxr, j = minc + 1; j <= maxc; j++) {
      oned[index] = arr[i][j];
      index++;
    }

    for (int i = maxr - 1, j = maxc; i >= minr; i--) {
      oned[index] = arr[i][j];
      index++;
    }

    for (int i = minr, j = maxc - 1; j > minc; j--) {
      oned[index] = arr[i][j];
      index++;
    }

    return oned;
  }

  public static void fillShellFromOned(int[][] arr, int s, int[] oned) {
    int minr = s - 1;
    int minc = s - 1;
    int maxr = arr.length - s;
    int maxc = arr[0].length - s;

    int index = 0;
    for (int i = minr, j = minc; i <= maxr; i++) {
      arr[i][j] = oned[index];
      index++;
    }

    for (int i = maxr, j = minc + 1; j <= maxc; j++) {
      arr[i][j] = oned[index];
      index++;
    }

    for (int i = maxr - 1, j = maxc; i >= minr; i--) {
      arr[i][j] = oned[index];
      index++;
    }

    for (int i = minr, j = maxc - 1; j > minc; j--) {
      arr[i][j] = oned[index];
      index++;
    }
  }

  public static void display(int[][] arr) {
    for (int i = 0; i < arr.length; i++) {
      for (int j = 0; j < arr[0].length; j++) {
        System.out.print(arr[i][j] + " ");
      }
      System.out.println();
    }
  }

}
# 7.the state of wakanda 2 -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int[][] arr = new int[n][n];
        for(int i=0; i<arr.length; i++)
        {
         for(int j=0; j<arr[0].length; j++)
         {
            arr[i][j] = scn.nextInt();
         }   
        }
        for(int g=0; g<arr.length; g++)
        {
           for(int i=0,j=g; j<arr.length; i++,j++)
           {
               System.out.println(arr[i][j]);
           } 
        }
    
    }

}
# 8.saddle price -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int[][] arr = new int[n][n];
        for(int i=0; i<arr.length; i++)
        {
         for(int j=0; j<arr[0].length; j++)
         {
            arr[i][j] = scn.nextInt();
         }   
        }
     for(int i=0; i<arr.length; i++)
     {   
         int svj=0;
         for(int j=1; j<arr[0].length; j++)
         {
            if(arr[i][j]<arr[i][svj])
            {
               svj=j;
            }
         }
         boolean flag = true;
         for(int k=0; k<arr.length; k++)
         {
             if(arr[k][svj]>arr[i][svj])
             {
                flag = false;
                break; 
             }
         }
        if(flag==true) 
        {
            System.out.println(arr[i][svj]);
            return;
        }
     }
     System.out.println("Invalid input");
    }

}
# 9.search in a sorted 2d array -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
       Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int[][] arr = new int[n][n];
        for(int i=0; i<arr.length; i++)
        {
         for(int j=0; j<arr[0].length; j++)
         {
            arr[i][j] = scn.nextInt();
         }   
        } 
       int x = scn.nextInt();
       int i = 0;
       int j = arr.length-1;
       while(i<arr.length && j>=0)
       {
           if(x==arr[i][j])
           {
             System.out.println(i);
             System.out.println(j);
             return;
           }
           else if(x<arr[i][j])
           {
               j--;
           }
           else if(x>arr[i][j])
           {
               i++;
           }
       }
       System.out.println("Not Found");
    }

}


# extra tips and points -->



