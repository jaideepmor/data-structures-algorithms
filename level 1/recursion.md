# ***** recursion --> 
                     syntax - string - 1.declare --> String str = "DSA";
                                       2.print --> System.out.println(str);
                                       3.character --> char ch = str.charAt(0);
                                       4.print each element --> for(int i=0; i<str.length(); i++){
                                                  char ch = str.charAt(i);
                                                  System.out.println(ch);
                                                 }
                                       5.substring --> String ss = str.substring(0,end point);

                            - array list - 1.declare --> ArrayList<Integer> list = new ArrayList<>();
                                           2.print --> System.out.println(list);
                                           3.size --> System.out.println(list.size());
                                           4.listadd(90);
                                           5.print each element --> for(int val : list){
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
 # 1. print decreasing -
 import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
      Scanner scn = new Scanner(System.in);
      int n = scn.nextInt();
      printdecreasing(n);
    }

    public static void printdecreasing(int n){
        if(n==0){
            return;
        }
        System.out.println(n);
        printdecreasing(n-1);
    }

}
 # 2. print increasing -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        printIncreasing(n);
    }

    public static void printIncreasing(int n){
        if(n==0){
        return;
        }
        printIncreasing(n-1);
        System.out.println(n);
    }

}
 # 3. print decreasing increasing - 
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    pdi(n);
    }

    public static void pdi(int n){
        if(n==0){
            return;
        }
        System.out.println(n);
        pdi(n-1);
        System.out.println(n);    
    }


}
 # 4. factorial -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int f = factorial(n); 
        System.out.println(f);
    }

    public static int factorial(int n){
        if(n==1){
            return 1;
        }
        int fn_1 = factorial(n-1);
        int fn = n*fn_1;
        return fn;
        }

}
 # 5. power(x,n) -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
     int x = scn.nextInt();
     int n = scn.nextInt();
     int xn = power(x,n);
     System.out.println(xn);
    }

    public static int power(int x, int n){
        if(n==0){
            return 1;
        }
        int xnm1 = power(x,n-1) ;
        int xn = x*xnm1;
        return xn;
    }

}
 # 6. power(2nd method) -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
       Scanner scn = new Scanner(System.in);
     int x = scn.nextInt();
     int n = scn.nextInt();
     int xn = power(x,n);
     System.out.println(xn);
    }

    public static int power(int x, int n){
        if(n==0){
            return 1;
        }
        int xpnb2 = power(x,n/2);
        int xn = xpnb2*xpnb2; 
        if(n%2==1){
         xn = xpnb2*xpnb2*x;
        }
        return xn;
    }

}
 # 7. print zigzag - 
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt(); 
        pzz(n);
        }

    public static void pzz(int n){
        if(n==0){
            return;
        }
        System.out.print(n+" ");
        pzz(n-1);
        System.out.print(n+" ");
        pzz(n-1);
        System.out.print(n+" ");
    }

}
 # 8. tower of hanoi -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int t1id = scn.nextInt();
        int t2id = scn.nextInt();
        int t3id = scn.nextInt();
        toh(n,t1id,t2id,t3id);
    }

    public static void toh(int n, int t1id, int t2id, int t3id){
        if(n==0){
            return;
        }
        toh(n-1,t1id,t3id,t2id);
        System.out.println(n + "[" + t1id + " -> " + t2id + "]");
        toh(n-1,t3id,t2id,t1id);  
    }

}
 # 9. display an array - 
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<arr.length; i++){
            arr[i] = scn.nextInt();
        }
        displayArr(arr,0);
    }

    public static void displayArr(int[] arr, int idx){
        if(idx==arr.length){
            return;
        }
        System.out.println(arr[idx]);
        displayArr(arr,idx+1);
    }

}
 # 10. display array in reverse -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<arr.length; i++){
            arr[i] = scn.nextInt();
        }
        displayArrReverse(arr,0);
    }

    public static void displayArrReverse(int[] arr, int idx){
        if(idx==arr.length){
            return;
        }
        displayArrReverse(arr,idx+1);
        System.out.println(arr[idx]);
        
    }

}
 # 11. max of an array - 
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<arr.length; i++){
            arr[i] = scn.nextInt();
        }
     int max = maxOfArray(arr,0);
       System.out.println(max);
    }

    public static int maxOfArray(int[] arr, int idx){
       if(idx==arr.length-1){
           return arr[idx];
       }
       int misa = maxOfArray(arr,idx+1);
        if(misa>arr[idx]){
            return misa;
        }else{
            return arr[idx];
        }
    }

}
 # 12. first index - 
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
      Scanner scn = new Scanner(System.in);
      int n = scn.nextInt();
      int[] arr = new int[n];
      for(int i=0; i<arr.length; i++){
          arr[i] = scn.nextInt();
      } 
      int d = scn.nextInt();
      int fi = firstIndex(arr,0,d);
      System.out.println(fi);
    }

    public static int firstIndex(int[] arr, int idx, int x){
        if(idx==arr.length){
            return -1;
        }
         if(arr[idx]==x){
            return idx;
        }else{
            int fiisa = firstIndex(arr,idx+1,x);
            return fiisa;
        }
        
       
    }

}
 # 13. last index -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
      Scanner scn = new Scanner(System.in);
      int n = scn.nextInt();
      int[] arr = new int[n];
      for(int i=0; i<arr.length; i++){
          arr[i] = scn.nextInt();
      } 
      int x = scn.nextInt();
      int li = lastIndex(arr,0,x);
      System.out.println(li);
    }

    public static int lastIndex(int[] arr, int idx, int x){
        if(idx==arr.length){
            return -1;
        }
      int liisa = lastIndex(arr,idx+1,x);
      if(liisa==-1){
          if(arr[idx]==x){
              return idx;
          }else{
              return -1;
          }
      }     
       else{
           return liisa;
       }
    }

}
 # 14. all indices of array -
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int n =

    int[] arr = new int[n];

    for (int i = 0; i < n; i++) {
      arr[i] = scn.nextInt();
    }
    int x = scn.nextInt();
    int[] iarr = allIndices(arr, x, 0, 0);

    if (iarr.length == 0) {
      System.out.println();
      return;
    }

    for (int i = 0; i < iarr.length; i++) {
      System.out.println(iarr[i]);
    }
  }

  public static int[] allIndices(int[] arr, int x, int idx, int fsf) {
    if (idx == arr.length) {
      return new int[fsf];
    }

    int[] iarr;

    if (arr[idx] == x) {
      iarr = allIndices(arr, x, idx + 1, fsf + 1);
      iarr[fsf] = idx;
    } else {
      iarr = allIndices(arr, x, idx + 1, fsf);
    }

    return iarr;
  }

}
 # 15.get subsequence - diff between - subsequence(2^n)- delete letter & substring(n(n+1)/2)- continouos or single combination - 
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    String str = scn.next();
    ArrayList< String> res = gss(str);
    System.out.println(res);
  }

  //bc ->  [ --,-c ,b-, bc ]
  //abc->  [ ---,--c, -b-, -bc, a--,ab-,abc]

  public static ArrayList< String> gss(String str) {
    if (str.length() == 0) {
      ArrayList< String> bres = new ArrayList< >();           //1
      bres.add("");
      return base;
    }
    char ch = str.charAt(0);                                      //2
    String ros = str.substring(1);                                //3

    ArrayList< String> rres = gss(ros);                            //4
    ArrayList< String> mres = new ArrayList< >();                   //5
    for (String val : rres) {
      mres.add("" + val);                                       //6
    }
    for (String val : rres) {
      mres.add(ch + val);                                       //7
    }

    return mres;                                                  //8
  }

}
 # 16.get keypad combination -
import java.io.*;
import java.util.*;
public class Main {
  public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    String str = scn.next();
    ArrayList< String> words = getKPC(str);
    System.out.println(words);
  }
  static String[] codes = {".;", "abc", "def", "ghi", "jkl", "mno", "pqrs", "tu", "vwx","yz"};                                                        //#
 
  public static ArrayList< String> getKPC(String str) {
    if (str.length() == 0) {                                  //1
      ArrayList< String>bres = new ArrayList< >();
      bres.add("");
      return bres;
    }
 
    char ch = str.charAt(0);                                      //2
    String ros = str.substring(1);                                //3
    ArrayList< String>rres = getKPC(bc);                           //4
    ArrayList< String> mres = new ArrayList< >();
 
    String codeforch = codes[ch - "0"];                           //5
 
    for (int i = 0; i < codeforch.length(); i++) {
      char chcode = codeforch.charAt(i);
      for (String val : rres) {                                   //6
        mres.add(chcode + val);
      }
    }
    return mres;                                                  //7
  }
 
}
 # 17.get stair paths -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    ArrayList<String> paths = getStairPaths(n);
    System.out.println(paths);
    }

    public static ArrayList<String> getStairPaths(int n) {
        if(n==0){
        ArrayList<String> bres = new ArrayList<>();
        bres.add("");
        return bres;    
        }
        else if(n<0){
        ArrayList<String> bres = new ArrayList<>();
        return bres;
        }
        ArrayList<String> path1 = getStairPaths(n-1);
        ArrayList<String> path2 = getStairPaths(n-2);
        ArrayList<String> path3 = getStairPaths(n-3);
        ArrayList<String> paths  = new ArrayList<>();
        for(String s:path1){
            paths.add("1"+s);
        }
        for(String s:path2){
            paths.add("2"+s);
        }
        for(String s:path3){
            paths.add("3"+s);
        }
        return paths;    
    }

}
 # 18.get maze paths -
 import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int m = scn.nextInt();
        ArrayList<String> paths = getMazePaths(1,1,n,m);
        System.out.println(paths);

    }

    
    public static ArrayList<String> getMazePaths(int sr, int sc, int dr, int dc) {
        if(sr==dr && sc==dc){
            ArrayList<String> bres = new ArrayList<>();
            bres.add("");
            return bres;
        }

        ArrayList<String> paths = new ArrayList<String>();
        
        if(sc<dc){
            ArrayList<String> hpath = getMazePaths(sr,sc+1,dr,dc);
            for(String s: hpath){
                paths.add("h"+s);
            }
        }

        if(sr<dr){
            ArrayList<String> vpath = getMazePaths(sr+1,sc,dr,dc);
            for(String s: vpath){
                paths.add("v"+s);
            }
        }
        
        return paths;
    }

}
 # 19.get maze paths with jumps -
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) throws Exception {

    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int m = scn.nextInt();

    ArrayList< String> paths = getMazePaths(1, 1, n, m);

    System.out.println(paths);
  }

  
  public static ArrayList< String> getMazePaths(int sr, int sc, int dr, int dc) {

    if (sr == dr && sc == dc)
    {
      ArrayList< String> bres = new ArrayList< >();
      bres.add("");
      return bres;
    }
    else if (sr > dr || sc > dc)
    {
      ArrayList< String> bres = new ArrayList< >();
      return bres;
    }

    ArrayList< String> paths = new ArrayList< >();
    for (int hms = 1; hms <= dc - sc; hms++)
    {
      ArrayList< String> hpaths = getMazePaths(sr, sc + hms, dr, dc);

      for (String hpath : hpaths)
      {
        paths.add("h" + hms + hpath);
      }
    }

    for (int vms = 1; vms <= dr - sr; vms++)
    {
      ArrayList< String> vpaths = getMazePaths(sr + vms, sc, dr, dc);

      for (String vpath : vpaths) {
        paths.add("v" + vms + vpath);
      }
    }

    for (int dms = 1; dms <= dr - sr && dms <= dc - sc; dms++)
    {
      ArrayList< String> dpaths = getMazePaths(sr + dms, sc + dms, dr, dc);

      for (String dpath : dpaths)    {
        paths.add("d" + dms + dpath);
      }
    }
    return paths;
  }
}
 # 20.print subsequence -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        String str = scn.nextLine();
        printSS(str,"");
        System.out.println();

    }

    public static void printSS(String que, String ans) {
        if(que.length()==0){       
           System.out.println(ans);
           return;
        }
        char ch = que.charAt(0);
        String res = que.substring(1);
         printSS(res,ans+ch);
         printSS(res,ans+"");
       
    }

}
 # 21.print keypad combination -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        String str = scn.next();
        printKPC(str,"");
    }
    static String[] codes = {".;","abc","def","ghi","jkl","mno","pqrs","tu","vwx","yz"};

    public static void printKPC(String que, String ans) {
     if(que.length()==0){
         System.out.println(ans);
         return;
     }
     char ch = que.charAt(0);
     String res = que.substring(1);
     String codesforch = codes[ch-'0'];
     for(int i=0; i<codesforch.length();i++){
         char option = codesforch.charAt(i);
          printKPC(res,ans+option);
     }
    }

}
 # 22.print stair paths -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        printStairPaths(n,"");

    }

    public static void printStairPaths(int n, String path) {
        if(n<0){
            return;
        }
        if(n==0){
            System.out.println(path);
            return;
        }
        printStairPaths(n-1,path+"1");
        printStairPaths(n-2,path+"2");
        printStairPaths(n-3,path+"3");
    }

}
 # 23.print maze paths -
import java.io.*;
	import java.util.*;

	public class Main {

	    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
		int n = scn.nextInt();
		int m = scn.nextInt();
		printMazePaths(1,1,n,m,"");
	    }

	    public static void printMazePaths(int sr, int sc, int dr, int dc, String psf) {
	        if(sr>dr||sc>dc){
				return;
			}
			if(sr==dr&&sc==dc){
				System.out.println(psf);
				return;
			}
			printMazePaths(sr,sc+1,dr,dc,psf+"h");
			printMazePaths(sr+1,sc,dr,dc,psf+"v");
	    }

	}
 # 24.print maze paths with jumps -
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int m = scn.nextInt();
    printMazePaths(1,1,n,m,"");
    }

  
    public static void printMazePaths(int sr, int sc, int dr, int dc, String psf) {
        if(sr==dr&&sc==dc){
            System.out.println(psf);
            return;
        }
        for(int ms=1; ms<=dc-sc; ms++){
            printMazePaths(sr,sc+ms,dr,dc,psf+"h"+ms);
        }
        for(int ms=1; ms<=dr-sr; ms++){
            printMazePaths(sr+ms,sc,dr,dc,psf+"v"+ms);
        }
           for(int ms=1; ms<=dr-sr && ms<=dc-sc; ms++){
            printMazePaths(sr+ms,sc+ms,dr,dc,psf+"d"+ms);
        }
    }

}
 # 25.print permuattions - 
import java.io.*;
 
import java.util.*;
 
public class Main {
 
  public static void main(String[] args) throws Exception {
 
    Scanner scn = new Scanner(System.in);
    String str = scn.next();
 
    printPermutations(str, "");
 
  }
 
  public static void printPermutations(String str, String asf) {
 
    if (str.length() == 0)
    {
      System.out.println(asf); //Question string is empty so print the answer now and return
      return ;
    }
    //Extracting each character at a time from the question string and appending it to answer so far
    for (int i = 0; i < str.length(); i++)
    {
      char ch = str.charAt(i);
      String leftPart = str.substring(0, i); //Substring from 0 to i-1 (left to ch)
      String rightPart = str.substring(i + 1); //Substring from i+1 till end of String (right to ch)
      String roq = leftPart + rightPart; //Remaining string after extracting ch
      printPermutations(roq, asf + ch);
    }
 
  }
}
 # 26.print encodings -
import java.io.*;
 
import java.util.*;
 
public class Main {
 
  public static void main(String[] args) throws Exception {
    BufferedReader br = new BufferedReader(new
                                           InputStreamReader(System.in));
    String str = br.readLine();
    printEncodings(str, "");
  }
 
  public static void printEncodings(String ques, String ans) {
    if (ques.length() == 0) {
      System.out.println(ans);
      return;
    } else if (ques.length() == 1) {
      if (ques.charAt(0) == '0') {
        return;
      } else {
        String ch0 = ques.substring(0, 1);
        String roq0 = ques.substring(1);
        String code0 = (char)('a' +
                              (Integer.parseInt(ch0) - 1)) + "";
        printEncodings(roq0, ans + code0);
      }
    } else {
      if (ques.charAt(0) == '0') {
        return;
      } else {
        String ch0 = ques.substring(0, 1);
        String roq0 = ques.substring(1);
        String code0 = (char)('a' +
                              (Integer.parseInt(ch0) - 1)) + "";
        printEncodings(roq0, ans + code0);
 
        String ch01 = ques.substring(0, 2);
        String roq01 = ques.substring(2);
        String code01 = (char)('a' +
                               (Integer.parseInt(ch01) - 1)) + "";
 
        if (Integer.parseInt(ch01) <= 26) {
          printEncodings(roq01, ans + code01);
        }
      }
    }
  }
}
 # 27.flood fill - 
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
    boolean[][] visited = new boolean[n][m];
    floodfill(arr, 0, 0, "", visited);
  }

  public static void floodfill(int[][] maze, int sr, int sc, String asf, boolean[][] visited) {
    if (sr < 0 || sc < 0 || sr == maze.length || sc == maze[0].length || maze[sr][sc] == 1 || visited[sr][sc] == true) {
      return;
    }
    if (sr == maze.length - 1 && sc == maze[0].length - 1) {
      System.out.println(asf);
      return;
    }
    visited[sr][sc] = true;
    floodfill(maze, sr - 1, sc, asf + "t", visited);
    floodfill(maze, sr, sc - 1, asf + "l", visited);
    floodfill(maze, sr + 1, sc, asf + "d", visited);
    floodfill(maze, sr, sc + 1, asf + "r", visited);
    visited[sr][sc] = false;


  }
 # 28.target sum subsets -
import java.io.*;
import java.util.*;
 
public class Main {
 
    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        int[] arr = new int[n];
    
        for(int i = 0; i < n; i++){
           arr[i] = Integer.parseInt(br.readLine());
        }
 
        int tar = Integer.parseInt(br.readLine());
        printTargetSumSubsets(arr, 0, "", 0, tar);
    }
 
    // set is the subset
    // sos is sum of subset
    // tar is target
    public static void printTargetSumSubsets(int[] arr, int idx, String set, int sos, int tar) {
        if(sos > tar){
            return;
        }
 
        if(idx == arr.length){
            if(sos == tar){
                System.out.println(set + ".");
            }
            return;
        }
 
        printTargetSumSubsets(arr, idx + 1, set + arr[idx] + ", ", sos + arr[idx], tar);
        printTargetSumSubsets(arr, idx + 1, set, sos, tar);
    }
 
}
 # 29.N queens -
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) throws Exception {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    int n = Integer.parseInt(br.readLine());
    int[][] chess = new int[n][n];
    printNQueens(chess, "", 0);
  }

  public static void printNQueens(int[][] chess, String qsf, int row) {
    if (row == chess.length) {
      System.out.println(qsf + ".");
      return;
    }
    for (int col = 0; col < chess.length; col++) {
      if (chess[row][col] == 0
          && isQueenSafe(chess, row, col) == true) {
        chess[row][col] = 1;
        printNQueens(chess,
                     qsf + row + "-" + col + ", ", row + 1);
        chess[row][col] = 0;
      }
    }
  }

  public static boolean isQueenSafe(int[][] chess,
                                    int row, int col) {
    for (int i = row - 1, j = col - 1;
         i >= 0 && j >= 0; i--, j--) {
      if (chess[i][j] == 1) {
        return false;
      }
    }

    for (int i = row - 1, j = col; i >= 0; i--) {
      if (chess[i][j] == 1) {
        return false;
      }
    }

    for (int i = row - 1, j = col + 1; i >= 0
         && j < chess.length; i--, j++) {
      if (chess[i][j] == 1) {
        return false;
      }
    }

    for (int i = row, j = col - 1; j >= 0; j--) {
      if (chess[i][j] == 1) {
        return false;
      }
    }

    return true;
  }
}
 # 30.knights tour -
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) throws Exception {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    int n = Integer.parseInt(br.readLine());
    int[][] chess = new int[n][n];
    printNQueens(chess, "", 0);
  }

  public static void printNQueens(int[][] chess, String qsf, int row) {
    if (row == chess.length) {
      System.out.println(qsf + ".");
      return;
    }
    for (int col = 0; col < chess.length; col++) {
      if (chess[row][col] == 0 && isQueenSafe(chess, row, col) == true) {
        chess[row][col] = 1;
        printNQueens(chess,qsf + row + "-" + col + ", ", row + 1);
        chess[row][col] = 0;
      }
    }
  }

  public static boolean isQueenSafe(int[][] chess,int row, int col) {
    for (int i = row - 1, j = col - 1; i >= 0 && j >= 0; i--, j--) {
      if (chess[i][j] == 1) {
        return false;
      }
    }

    for (int i = row - 1, j = col; i >= 0; i--) {
      if (chess[i][j] == 1) {
        return false;
      }
    }

    for (int i = row - 1, j = col + 1; i >= 0
         && j < chess.length; i--, j++) {
      if (chess[i][j] == 1) {
        return false;
      }
    }

    for (int i = row, j = col - 1; j >= 0; j--) {
      if (chess[i][j] == 1) {
        return false;
      }
    }

    return true;
  }
}

 # extra questions and points --

