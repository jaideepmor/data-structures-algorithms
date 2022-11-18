# ***** Function and number system --> 
                             syntax -
                             public static int function(int x)                  
                                                              {int rv;
									  		
	
										                                           return rv;}
                                                          
   								
										   
                                
            




# questions --> 
# 1.digit frequency -modulus of a no.gives-reminder-current digit,division of a no.gives-carry-next digit.
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int d = scn.nextInt();
        int f = getDigitFrequency(n, d);
        System.out.println(f);
    }

    public static int getDigitFrequency(int n, int d) {
        int rvgdf = 0; 
        while(n>0){
        int dig = n%10;
        n = n/10;
         if(dig==d){
             rvgdf++;
         }
        }
        return rvgdf;

        
        
    }
}
# 2.decimal to any base - 
import java.util.*;
  
  public class Main{
  
  public static void main(String[] args) {
      Scanner scn = new Scanner(System.in);
      int n = scn.nextInt();
      int b = scn.nextInt();
      int dn = getValueInBase(n, b);
      System.out.println(dn);
   }
  
   public static int getValueInBase(int n, int b){
       int rv = 0; ;
       int p = 1;
       while(n > 0){
       int dig = n % b;
       n = n / b;
       
       rv += dig * p;    
       p = p * 10;
       }
        return rv ;
   }
  }
# 3.any base to decimal - 
import java.util.*;
  
  public class Main{
  
  public static void main(String[] args) {
      Scanner scn = new Scanner(System.in);
      int n = scn.nextInt();
      int b = scn.nextInt();
      int d = getValueIndecimal(n, b);
      System.out.println(d);
   }
  
   public static int getValueIndecimal(int n, int b){
      int rv = 0;
      int p = 1;
      while(n > 0){
         int dig = n % 10;
         n = n / 10;
         rv += dig * p;
         p = p * b;
      }
      return rv;
   }
  }
# 4.any base to any base -  
import java.io.*;
 
import java.util.*;
 
public class Main {
 
  public static void main(String[] args) {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int sourceBase = scn.nextInt();
    int  destBase = scn.nextInt();
 
    int res = getValue(n, sourceBase, destBase);
    System.out.println(res);
  }
  public static int getValue(int n, int b1, int b2) {
    int dec = getValueInDecimal(n, b1);
    int dn = getValueInBase(dec, b2);
    return dn;
  }
  public static int getValueInBase(int n, int b) {
    int rv = 0;
    int p = 1;
    while (n > 0) {
      int dig = n % b;
      n = n / b;
      rv = rv + (dig * p);
      p = p * 10;
    }
    return rv;
  
}
  public static int getValueInDecimal(int n, int b) {
    int rv = 0;
    int p = 1;
 
    while (n > 0) {
      int dig = n % 10;
      n = n / 10;
      rv = rv + (dig * p);
 
      p = p * b;
    }
    return rv;
  }
}
# 5.any base addition -
import java.util.*;
  
  public class Main{
  
  public static void main(String[] args) {
      Scanner scn = new Scanner(System.in);
      int b = scn.nextInt();
      int n1 = scn.nextInt();
      int n2 = scn.nextInt();
  
      int d = getSum(b, n1, n2);
      System.out.println(d);
   }
  
   public static int getSum(int b, int n1, int n2){
       int rv = 0;
       int c = 0;
       int p = 1;
       while(n1>0 || n2>0 || c>0){
           int d1 = n1%10;
           int d2 = n2%10;
           n1 = n1/10;
           n2 = n2/10;
          int d = d1 + d2 + c;
           c = d/b;
           d = d%b;
           rv+= d*p;
           p = p*10;
        }
    return rv;
   }
  }
# 6.any base subtraction -
import java.io.*;
 
import java.util.*;
 
public class Main {
 
  public static void main(String[] args) {
    Scanner scn = new Scanner(System.in);
    int b = scn.nextInt();
    int n1 = scn.nextInt();
    int n2 = scn.nextInt();
 
    int d = getDifference(b, n1, n2);
    System.out.println(d);
  }
 
  public static int getDifference(int b, int n1, int n2) {
    int rv = 0;
 
    int c = 0;
    int p = 1;
    while (n2 > 0) {
      int d1 = n1 % 10;
      int d2 = n2 % 10;
      n1 = n1 / 10;
      n2 = n2 / 10;
 
      int d = d2 - d1 - c;
 
      if (d < 0) {
        c = 1;
        d += b;
      } else {
        c = 0;
      }
 
      rv += d * p;
      p = p * 10;
    }
    return rv;
  }
}
# 7.any base multiplication - 
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) {
    Scanner scn = new Scanner(System.in);
    int b = scn.nextInt();
    int n1 = scn.nextInt();
    int n2 = scn.nextInt();

    int d = getProduct(b, n1, n2);
    System.out.println(d);
  }

  public static int getProduct(int b, int n1, int n2) {
    int rv = 0;

    int c = 0;
    int p = 1;
    while (n2 > 0) {
      int d2 = n2 % 10;
      n2 = n2 / 10;

      int pwd = getProductWithDigit(b, n1, d2);
      rv = getSum(b, rv, p * pwd);
      p = p * 10;
    }

    return rv;
  }

  public static int getProductWithDigit(int b, int n1, int d2) {
    int rv = 0;

    int c = 0;
    int p = 1;
    while (n1 > 0 || c > 0) {
      int d1 = n1 % 10;
      n1 = n1 / 10;

      int d = d1 * d2 + c;
      c = d / b;
      d = d % b;

      rv += d * p;
      p = p * 10;
    }

    return rv;
  }

  public static int getSum(int b, int n1, int n2) {
    int rv = 0;

    int c = 0;
    int p = 1;
    while (n1 > 0 || n2 > 0 || c > 0) {
      int d1 = n1 % 10;
      int d2 = n2 % 10;
      n1 = n1 / 10;
      n2 = n2 / 10;

      int d = d1 + d2 + c;
      c = d / b;
      d = d % b;

      rv += d * p;
      p = p * 10;
    }

    return rv;
  }
}
# any base division - 




# ***** Array -->     

                           introduction - syntax - int[] arr = new int[n]; or int[] arr; arr = new int[n];
							                                     arr[] = some value;
							                                     arr.length;
              imp. points    - int(primitive datatypes)-create memory in stack.
                             -  new - create memory in heap.
                             - array(non primitive datatypes) .

# questions - 
****** (counting starts from left = i = 0 upto right = j = n-1, n = array length)                                                 
# 1.span of array - 
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int[] arr = new int[n];

    for (int i = 0; i < n; i++) {
      arr[i] = scn.nextInt();
    }

    int min = arr[0];
    int max = arr[0];

    for (int i = 1; i < arr.length; i++) {
      if (arr[i] < min) {
        min = arr[i];
      }

      if (arr[i] > max) {
        max = arr[i];
      }
    }

    int span = max - min;
    System.out.println(span);
  }
}
# 2.find element in an array - 
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int[] arr = new int[n];

    for (int i = 0; i < n; i++) {
      arr[i] = scn.nextInt();
    }

    int d = scn.nextInt();

    for (int i = 0; i < arr.length; i++) {
      if (d == arr[i]) {
        System.out.println(i);
        return;
      }
    }
    System.out.println(-1);
  }

}
# 3.bar chart - 
import java.io.*;
import java.util.*;

public class Main{

public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int[] arr = new int[n];
    for(int i=0; i<arr.length; i++){
        arr[i] = scn.nextInt();
    }
    int max = arr[0];
    for(int i=1; i<arr.length; i++){
        if(arr[i]>max){
           max=arr[i]; 
        }
    }
    for(int floor=max; floor>=1; floor--){
        for(int i=0; i<arr.length; i++){
         if(arr[i]>=floor){
            System.out.print("*\t");
         }
         else{
            System.out.print("\t"); 
         }   
        }
        System.out.println();
    }

    
 }

}
# 4.sum of array -  
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);

    int n1 = scn.nextInt();
    int[] a1 = new int[n1];
    for(int i=0; i<a1.length; i++)
    { a1[i] = scn.nextInt(); }

    int n2 = scn.nextInt();
    int[] a2 = new int[n2];
    for(int i=0; i<a2.length; i++)
    { a2[i] = scn.nextInt(); }

    int[] sum = new int[n1 > n2 ? n1 : n2];
    int i = n1 - 1;
    int j = n2 - 1;
    int k = sum.length - 1;
    int c = 0;
    while (k >= 0) {
      int d = c;

      if (i >= 0)
        d += a1[i];

      if (j >= 0)
        d += a2[j];

      c = d / 10;
      d = d % 10;
      sum[k] = d;

      i--;
      j--;
      k--;
    }

    if (c > 0) {
      System.out.println(c);
    }
    for (int val : sum) {
      System.out.println(val);
    }
  }

}
# 5.difference of array - 
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) throws Exception {
    // write your code here
    Scanner scn = new Scanner(System.in);
    int n1 = scn.nextInt();
    int a1[] = new int[n1];

    for (int i = 0; i < a1.length; i++) {
      a1[i] = scn.nextInt();
    }

    int n2 = scn.nextInt();
    int a2[] = new int[n2];

    for (int i = 0; i < a2.length; i++) {
      a2[i] = scn.nextInt();
    }

    int diff[] = new int[n2];
    int c = 0;
    int i = a1.length - 1;
    int j = a2.length - 1;
    int k = diff.length - 1;

    while (k >= 0) {
      int d = 0;
      int a1v = (i >= 0 ? a1[i] : 0);
      if (a2[j] + c >= a1v) {
        d = a2[j] + c - a1v;
        c = 0;
      } else {
        d = a2[j] + 10 + c - a1v;
        c = -1;
      }

      diff[k] = d;
      i--;
      j--;
      k--;
    }

    int idx = 0;
    while (idx < diff.length && diff[idx] == 0) {
      idx++;
    }

    while (idx < diff.length) {
      System.out.println(diff[idx++]);

    }
  }
}
# 6.reverse of an array - swap left half and right half with each other from middle section.
import java.io.*;
import java.util.*;

public class Main{
  public static void display(int[] a){
    StringBuilder sb = new StringBuilder();

    for(int val: a){
      sb.append(val + " ");
    }
    System.out.println(sb);
  }

  public static void reverse(int[] a){
                    int i = 0;
                    int j = a.length-1;
                    while(i<j)
                    { int temp = a[i];
                          a[i] = a[j];
                          a[j] = temp;
                      i++;
                      j--;
                    }
  }

public static void main(String[] args) throws Exception {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

    int n = Integer.parseInt(br.readLine());
    int[] a = new int[n];
    for(int i = 0; i < n; i++){
       a[i] = Integer.parseInt(br.readLine());
    }

    reverse(a);
    display(a);
 }

}
# 7.rotate an array - handle 3 case - rotate - -ve,+ve,>>>>no.,reverse-part1,part2 and whole Arr.-swap.
import java.io.*;
import java.util.*;

public class Main{
  public static void display(int[] a){
    StringBuilder sb = new StringBuilder();

    for(int val: a){
      sb.append(val + " ");
    }
    System.out.println(sb);
  }
   
  public static void reverse(int[] a, int i,int j)
  {
    int l = i;
    int r = j;
    while(l<r)
    { int temp = a[l];
      a[l] = a[r];
      a[r] = temp;
      l++;
      r--;
    }
   }


  public static void rotate(int[] a, int k){
    k = k % a.length;
    if(k<0)
    {
      k = k + a.length;
    }
    reverse(a,0,a.length-k-1);
    reverse(a,a.length-k,a.length-1);
    reverse(a,0,a.length-1); 
   }

public static void main(String[] args) throws Exception {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

    int n = Integer.parseInt(br.readLine());
    int[] a = new int[n];
    for(int i = 0; i < n; i++){
       a[i] = Integer.parseInt(br.readLine());
    }
    int k = Integer.parseInt(br.readLine());

    rotate(a, k);
    display(a);
 }

}
# 8.inverse of an array - interchange - value with position .
import java.io.*;
import java.util.*;

public class Main{
  public static void display(int[] a){
    StringBuilder sb = new StringBuilder();

    for(int val: a){
      sb.append(val + "\n");
    }
    System.out.println(sb);
  }

  public static int[] inverse(int[] a){
    int[] inv = new int[a.length];
    for(int i=0; i<a.length; i++)
    { int v = a[i]; 
      inv[v] = i;
    }
    return inv;
  }

public static void main(String[] args) throws Exception {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

    int n = Integer.parseInt(br.readLine());
    int[] a = new int[n];
    for(int i = 0; i < n; i++){
       a[i] = Integer.parseInt(br.readLine());
    }

    int[] inv = inverse(a);
    display(inv);
 }

}
# 9.subarray problem - 3 - loops - i,j,k,right angle triangles  figures will form,i st. from 0,j is at i ,then k travel from i to j.
import java.io.*;
import java.util.*;

public class Main{

public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int[] a = new int[n];
    for(int i=0; i<a.length; i++)
    { a[i] = scn.nextInt(); }  
    for(int i=0; i<a.length; i++)
    {
        for(int j=i; j<a.length; j++)
        {
            for(int k=i; k<=j; k++)
            {
             System.out.print(a[k]+"\t");
            }
            System.out.println();
        }
    }
     
     
 }

}
# 10.subsets of array - loop length - 2^n subsets, binary number system representation,divide upto a[] length.
import java.io.*;
import java.util.*;

public class Main{

public static void main(String[] args) throws Exception {
       Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int[] a = new int[n];
    for(int i=0; i<a.length; i++)
    { a[i] = scn.nextInt(); }  
    int limit = (int)Math.pow(2,a.length);
    for(int i=0; i<limit; i++)
    {  String subsets = "";
    int temp = i;
       for(int j=a.length-1; j>=0; j--)
       { 
          int r = temp%2;
          temp = temp/2;
          if(r==0)
          {
           subsets = "-\t"+subsets;
          }else
          {
           subsets = a[j]+"\t"+subsets;
          }

       }
       System.out.println(subsets);
    }
   

    }

}

# ***** Binary search algorithm --> applicable for sorted array,set low,high and middle limit= (l+h)/2,search,change the limit until u find the number. 

# questions - 
# 1.Broken economy - ceil and floor - set value of low,high,condition,middle,ceil,floor,change their values acc. to 3 conditions.
import java.io.*;
import java.util.*;

public class Main{

public static void main(String[] args) throws Exception {
     Scanner scn = new Scanner(System.in);
     int n = scn.nextInt();
     int[] arr = new int[n];
     for(int i=0; i<arr.length; i++)
     {
         arr[i] = scn.nextInt();
     }
     int data = scn.nextInt();
     int low = 0;
     int high = arr.length-1;
     int floor = 0;
     int ceil = 0;
     while(low<=high)
     {  
         int middle = (low+high)/2;
         if(data<arr[middle])
         {
            high = middle-1;
            ceil = arr[middle];
         }
         else if(data>arr[middle])
         {
           low = middle+1; 
           floor = arr[middle]; 
         }
         else
         { 
           floor = arr[middle];
           ceil = arr[middle];
           break;
         }

     } 
     System.out.println(ceil);
     System.out.println(floor);
 }

}
# 2.1st index and last index - same as binary search algo. with further steps of either going forward or backward depending on 1st and last index.
import java.io.*;
import java.util.*;

public class Main{

public static void main(String[] args) throws Exception {
     Scanner scn = new Scanner(System.in);
     int n = scn.nextInt();
     int[] arr = new int[n];
     for(int i=0; i<arr.length; i++)
     {
         arr[i] = scn.nextInt();
     }
     int data = scn.nextInt();
     int low = 0;
     int high = arr.length-1;
     int first = -1;
     while(low<=high)
     {  
         int middle = (low+high)/2;
         if(data<arr[middle])
         {
            high = middle-1;
         }
         else if(data>arr[middle])
         {
           low = middle+1;  
         }
         else
         { 
           first = middle;
           high = middle-1;
         }

     } 
     System.out.println(first);
     
      low = 0;
      high = arr.length-1;
     int last = -1;
     while(low<=high)
     {  
         int middle = (low+high)/2;
         if(data<arr[middle])
         {
            high = middle-1;
         }
         else if(data>arr[middle])
         {
           low = middle+1;  
         }
         else
         { 
           last = middle;
           low = middle+1;
         }

     } 
     System.out.println(last);
 }

}

# extra points and tips -->