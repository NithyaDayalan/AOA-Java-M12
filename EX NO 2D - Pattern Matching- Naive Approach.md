# EX 2D Pattern Matching using Naive Approach.
## AIM:
To write a Java program to for given constraints.
Given text string with length n and a pattern with length m, the task is to prints all occurrences of pattern in text.
Note: You may assume that n > m.

Examples: 

Input:  text = "THIS IS A TEST TEXT", pattern = "TEST"
Output: Pattern found at index 10

Input:  text =  "AABAACAADAABAABA", pattern = "AABA"
Output: Pattern found at index 0, Pattern found at index 9, Pattern found at index 12
## Algorithm:
1. Read the text and the pattern from the user.
2. Loop through each possible starting index in the text.
3. Compare the pattern with the substring of the text character by character.
4. If all characters match, print the starting index of the match.
5. Continue until the end of the text is reached.

## Program:
```
Developed by: NITHYA D
Register Number: 212223240110
```
```
import java.util.Scanner;

public class NaivePatternSearch {
    static void search(String text, String pattern) {
        int n = text.length();
        int m = pattern.length();

        for (int i = 0; i <= n - m; i++) {
            int j;

            // Check for pattern match character by character
            for (j = 0; j < m; j++) {
                if (text.charAt(i + j) != pattern.charAt(j))
                    break;
            }

            // If pattern found
            if (j == m)
                System.out.println("Pattern found at index " + i);
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Taking input from the user
        //System.out.print("Enter the text: ");
        String text = scanner.nextLine();

        //System.out.print("Enter the pattern: ");
        String pattern = scanner.nextLine();

        // Search for pattern in the text
        search(text, pattern);

        scanner.close();
    }
}
```

## Output:
<img width="735" height="247" alt="image" src="https://github.com/user-attachments/assets/75b31c7b-d554-4882-b385-b61818fdf7c9" />

## Result:
The program successfully implemented and the expected output is verified.
