# EX 2E Pattern Matching using KMP Algorithm.
## AIM:
To write a Java program for the following constraints.
Longest Palindromic Substring
Given a string s, return the longest palindromic substring in s.
using Manacher's Algorithm

## Algorithm:
1. Read the number of test cases.
2. For each test case, read the text and pattern.
3. Loop through the text and compare substrings with the pattern character by character.
4. Store the starting indices where the pattern matches; if none, store -1.
5. Print the list of indices for each test case.  

## Program:
```
Developed by: NITHYA D
Register Number: 212223240110 
```
```
import java.util.*;

public class PatternMatching {

    public static List<Integer> findPatternIndices(String text, String pattern) {
        List<Integer> result = new ArrayList<>();
        int n = text.length();
        int m = pattern.length();

        for (int i = 0; i <= n - m; i++) {
            int j;
            for (j = 0; j < m; j++) {
                if (text.charAt(i + j) != pattern.charAt(j)) {
                    break;
                }
            }
            if (j == m) {
                result.add(i);
            }
        }

        if (result.isEmpty()) {
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
```

## Output:
<img width="695" height="269" alt="image" src="https://github.com/user-attachments/assets/a60c4700-99d3-4143-9f73-0c3bc0245aaf" />

## Result:
The program successfully implemented and the expected output is verified.
