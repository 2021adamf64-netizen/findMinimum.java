# findMinimum.java
This program inputs a series of random number and checks to see the minimum of those numbers
import java.util.Scanner;
public class findMinimum {

    // Method 1: Minimum of two integers
    public static int findMinimum(int a, int b) {
        return (a < b) ? a : b;
    }

    // Method 2: Minimum of three integers
    public static int findMinimum(int a, int b, int c) {
        return Math.min(a, Math.min(b, c));
    }

    // Method 3: Alphabetical comparison of two words
    // Returns 1 if word1 comes first, 2 if word2 comes first
    public static int findMinimum(String word1, String word2) {
        if (word1.compareToIgnoreCase(word2) < 0) {
            return 1;
        } else {
            return 2;
        }
    }

    // Main method to test all three overloaded methods
    public static void main(String[] args) {
        // Test: Minimum of two integers
		Scanner scnr = new Scanner(System.in);
		System.out.print("Enter a:");
		int anum = scnr.nextInt();
		System.out.print("Enter b:");
		int bnum = scnr.nextInt();
		System.out.print("Enter c:");
		int cnum = scnr.nextInt();
		System.out.print("Enter word 1:");
		String worder1 = scnr.nextLine();
		System.out.println("Enter word 2:");
		String worder2 = scnr.nextLine();
        int minTwo = findMinimum(anum, bnum);
        System.out.println("Minimum of" + anum + "and" + bnum + "is:" + minTwo);

        // Test: Minimum of three integers
        int minThree = findMinimum(anum, bnum, cnum);
        System.out.println("Minimum of" + anum + "," + bnum + "," + "and" + cnum + "is:" + minThree);

        // Test: Alphabetical comparison
        int result = findMinimum(worder1, worder2);
        if (result == 1) {
            System.out.println("The first word (worder1) comes first alphabetically.");
        } else {
            System.out.println("The second word (worder2) comes first alphabetically.");
        }
    }
}
