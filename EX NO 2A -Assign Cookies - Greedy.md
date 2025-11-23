# EX 2A Assign Cookies using Greedy Algorithm. 
## AIM:
To Write a Java program for the following Constraints.
Assume you are an awesome parent and want to give your children some cookies. But, you should give each child at most one cookie.

Each child i has a greed factor g[i], which is the minimum size of a cookie that the child will be content with; and each cookie j has a size s[j]. If s[j] >= g[i], we can assign the cookie j to the child i, and the child i will be content. Your goal is to maximise the number of your content children and output the maximum number.

## Algorithm:
1. Read the greed factors array g and cookie sizes array s.
2. Sort both arrays in ascending order.
3. Initialize two pointers for children and cookies.
4. Assign cookies to children if the cookie size is greater than or equal to the child's greed.
5. Count and print the number of children who got cookies.  

## Program:
```
Developed by: NITHYA D
Register Number: 2122223240110
```
```
import java.util.*;

public class AssignCookies {
    
    public static int findContentChildren(int[] g, int[] s) {
        Arrays.sort(g);
        Arrays.sort(s);
        int i = 0, j = 0;
        while (i < g.length && j < s.length) {
            if (s[j] >= g[i]) i++;
            j++;
        }
        return i;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] g = new int[n];
        for (int i = 0; i < n; i++) g[i] = sc.nextInt();
        int m = sc.nextInt();
        int[] s = new int[m];
        for (int i = 0; i < m; i++) s[i] = sc.nextInt();
        System.out.println(findContentChildren(g, s));
    }
}
```
## Output:
<img width="562" height="314" alt="image" src="https://github.com/user-attachments/assets/0cf1073e-eaf3-4881-a3b7-b8209e485ca2" />

## Result:
The program successfully print all the numbers from 1 to N. 
