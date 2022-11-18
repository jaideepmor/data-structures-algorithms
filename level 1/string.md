# ***** String -->   syntax -- 
                                                     syntax - string - 1.declare --> String str = "DSA";
                                       2.print --> System.out.println(str);
                                       3.character --> char ch = str.charAt(0);
                                       4.length --> for(int i=0; i<str.length(); i++){
                                                  char ch = str.charAt(i);
                                                  System.out.println(ch);
                                                 }
                                       5.substring --> String ss = str.substring(0,end point);

                            - array list - 1.declare --> ArrayList<Integer> list = new ArrayList<>();
                                           2.print --> System.out.println(list);
                                           3.size --> System.out.println(list.size());
                                           4.list.add(90);
                                           5.print size --> for(int val : list){
                                                system.out.println(val);
                                           }
                                           or
                                             for(int i=0; i<list.size(); i++){
                                                 int val = list.get(i);
                                                System.out.println(val);
                                             }
                                           6. list.set(1,100);  
                                           7. list.add(1,100);
                                           

# questions -- 
# 1.print all palindromic substrings -
import java.io.*;

import java.util.*;

public class Main {

  public static void solution(String str) {
    for (int i = 0 ; i < str.length(); i++) {
      for (int j = i + 1; j <= str.length(); j++) {

        if (isPalindrome(str.substring(i, j))) {
          System.out.println(str.substring(i, j));
        }
      }
    }
  }

  public static boolean isPalindrome(String str) {
    int i = 0, j = str.length() - 1;
    while (i < j) {
      if (str.charAt(i) != str.charAt(j)) {
        return false;
      }
      i++;
      j--;
    }
    return true;
  }
  public static void main(String[] args) {
    Scanner scn = new Scanner(System.in);
    String str = scn.next();
    solution(str);
  }

}
# 2.string compression -
import java.io.*;

import java.util.*;

public class Main {

  public static String compression1(String s) {
    String ans = "";
    for (int i = 0 ; i < s.length(); i++) {
      while (i < s.length() - 1 && s.charAt(i) == s.charAt(i + 1)) {
        i++;
      }
      ans += s.charAt(i);
    }
    return ans;
  }

  public static String compression2(String s) {
    String ans = "";
    for (int i = 0 ; i < s.length(); i++) {
      int count = 1;
      while (i < s.length() - 1
             && s.charAt(i) == s.charAt(i + 1)) {
        count++;
        i++;
      }
      ans += s.charAt(i);
      if (count > 1) {
        ans += count;
      }
    }
    return ans;
  }
  public static void main(String[] args) {
    Scanner scn = new Scanner(System.in);
    String s = scn.next();
    System.out.println(compression1(s));
    System.out.println(compression2(s));
  }
}
# 3.toggle optica document - 
import java.io.*;
import java.util.*;

public class Main {
	public static String toggleCase(String str){
	StringBuilder sb = new StringBuilder(str);
	for(int i=0; i<sb.length(); i++){
        char ch = sb.charAt(i);
        if(ch>='a'  && ch<='z'){
         char upch = (char)('A'+ch-'a');
		 sb.setCharAt(i,upch);
		}else if(ch>='A' && ch<='Z'){
		 char lwch = (char)('a'+ch-'A');
		 sb.setCharAt(i,lwch);	
		}
	 }
	 return sb.toString();
	
}
	
	public static void main(String[] args) {
		Scanner scn = new Scanner(System.in);
		String str = scn.next();
		System.out.println(toggleCase(str));
	}

}
# 4.string with difference of every two consecutive characters - 
import java.io.*;
import java.util.*;

public class Main {

	public static String solution(String str){
		StringBuilder sb = new StringBuilder();
		sb.append(str.charAt(0));
        
		for(int i=1; i<str.length(); i++){
			char c = str.charAt(i);
			char p = str.charAt(i-1);
			int gap = c-p;
            sb.append(gap);
			sb.append(c);
		}
		return sb.toString(); 
	}
	public static void main(String[] args) {
		Scanner scn = new Scanner(System.in);
		String str = scn.next();
		System.out.println(solution(str));
	}

}
# 5.remove primes -
import java.io.*;
import java.util.*;

public class Main {

	public static boolean isPrime(int val){
		for(int div=2; div*div<=val; div++){
          if(val%div==0){
			  return false;
		  }
		}
		return true;
	}

	public static void solution(ArrayList<Integer> al){
		for(int i=al.size()-1; i>=0; i--){
			int val=al.get(i);
			if(isPrime(val)==true){
             al.remove(i);
			}
		}
		
	}
	public static void main(String[] args) {
		Scanner scn = new Scanner(System.in);
		int n = scn.nextInt();
		ArrayList<Integer> al = new ArrayList<>();
		for(int i = 0 ; i < n; i++){
			al.add(scn.nextInt());
		}
		solution(al);
		System.out.println(al);
	}

}
# 6.print all permutations of a string iteratively -
import java.io.*;
import java.util.*;

public class Main {

	public static void solution(String str){
	int n=str.length();
	int f=factorial(n);
	for(int i=0; i<f; i++){
		StringBuilder sb = new StringBuilder(str);
		int temp=i;
        for(int div=n; div>=1; div--){
           int q=temp/div;
		   int r=temp%div;
        System.out.print(sb.charAt(r));
        sb.deleteCharAt(r);
		   temp=q;
		}
		System.out.println();
	}
		
	}

	public static int factorial(int n){
		int val=1;
		for(int i=2; i<=n; i++){
			val*=i;
		}
		return val;
    }

	public static void main(String[] args) {
		Scanner scn = new Scanner(System.in);
		String str = scn.next();
		solution(str);
	}

}

# extra tips and points -- 