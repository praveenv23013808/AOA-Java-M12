EX 2E Pattern Matching using KMP Algorithm.
DATE:09/10/25
AIM:
To write a Java program for the following constraints. Longest Palindromic Substring Given a string s, return the longest palindromic substring in s. using Manacher's Algorithm

Algorithm
Input number of test cases T
Repeat the following steps for each test case: Read the input text. Read the input pattern. Initialize an empty list result to store the starting indices of matches. n = length of text m = length of pattern
Slide the pattern over the text: For each position i from 0 to n - m: Compare each character of pattern with the substring of text starting at index i. Initialize j = 0. While j < m and text[i + j] == pattern[j], continue comparing. If all characters match (j == m), add index i to result.
Check if no match is found: If result is empty, add -1 to indicate that the pattern was not found.
Print all indices in result.
Program:
/*
Program to implement Reverse a String
Developed by: Dhiyaneshwar P
Register Number:212222110009
import java.util.*;

public class PatternMatching {

    public static List<Integer> findPatternIndices(String text, String pattern) {
       //Type code here...
       List<Integer>result=new ArrayList<>();
       int n=text.length();
       int m=pattern.length();
       for(int i=0;i<=n-m;i++){
           int j;
           for(j=0;j<m;j++){
               if(text.charAt(i+j)!=pattern.charAt(j)){
                   break;
               }
           }
           if(j==m){
               result.add(i);
           }
       }
       if(result.isEmpty()){
           result.add(-1);
       }
       return result;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int T = Integer.parseInt(scanner.nextLine()); // number of test cases

        for (int t = 0; t < T; t++) {
            String text = scanner.nextLine();
            String pattern = scanner.nextLine();

            List<Integer> indices = findPatternIndices(text, pattern);
            for (int idx : indices) {
                System.out.print(idx + " ");
            }
            System.out.println();
        }

        scanner.close();
    }
}
  
*/
Output:
image
Result:
The program successfully implemented and the expected output is verified.
