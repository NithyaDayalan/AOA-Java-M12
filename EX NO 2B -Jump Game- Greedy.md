# EX 2B Jump Game using Greedy Algorithm.
## AIM:
To write a Java program to for given constraints.
You are given an array of integers. Each number represents the maximum number of steps you can jump forward from that position.

You start from the first element (index 0). 
Write a program to find the minimum number of jumps required to reach the last index of the array.

If it is not possible to reach the end, return -1.

## Algorithm:
1. Read the size of the array and its elements from the user.
2. Initialize a variable to track the farthest reachable index.
3. Iterate through the array.
4. If the current index is beyond the reachable index, return false. 
5. Update the reachable index and print true if the last index can be reached. 

## Program:
```
Developed by: NITHYA D
Register Number: 212223240110
```
```
import java.util.Scanner;

public class JumpGame {

    // Function to check if we can reach the last index
    public static boolean canReachLastIndex(int[] nums) {
        int reachable = 0;
        for (int i = 0; i < nums.length; i++) {
            if (i > reachable) {
                return false;
            }
            reachable = Math.max(reachable, i + nums[i]);
        }
        return true;
    }

    // Main method for input and calling the function
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); // Size of array
        int[] nums = new int[n];
        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt(); // Elements of array
        }

        System.out.println("Can reach last index: " + canReachLastIndex(nums));
    }
}
```

## Output:
<img width="731" height="225" alt="image" src="https://github.com/user-attachments/assets/fc2d29dc-9d9b-412b-9178-bc37a901d4e6" />

## Result:
The program successfully implemented and the expected output is verified.
