import java.util.Scanner;


public class StudentMarksAverage {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double[] marks = new double[5];
        double total = 0.0;

        System.out.println("Enter the marks for the five units:");

        for (int x = 0; x < 5; x++) {
            System.out.print("Mark for unit " + (x + 1) + ": ");
            marks[x] = scanner.nextDouble();
            total += marks[x];
        }

        double average = total / 5;

        System.out.printf("The average mark is: %.2f%n", average);

        scanner.close();
    }
}

public class DivisibilityTest {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an integer: ");
        int number = scanner.nextInt();

        System.out.println("Divisibility test results for number " + number + ":");

        for (int y = 1; y <= 9; y++) {
            if (isDivisible(number, y)) {
                switch (y) {
                    case 2:
                        System.out.println("The number is divisible by 2 because it is even.");
                        break;
                    case 3:
                        System.out.println("The number is divisible by 3 because the sum of its digits is divisible by 3.");
                        break;
                    case 4:
                        System.out.println("The number is divisible by 4 because the last two digits form a number divisible by 4.");
                        break;
                    case 5:
                        System.out.println("The number is divisible by 5 because it ends with a 0 or 5.");
                        break;
                    case 6:
                        System.out.println("The number is divisible by 6 because it is divisible by both 2 and 3.");
                        break;
                    case 7:
                        System.out.println("The number is divisible by 7 (special rule).");
                        break;
                    case 8:
                        System.out.println("The number is divisible by 8 because the last three digits form a number divisible by 8.");
                        break;
                    case 9:
                        System.out.println("The number is divisible by 9 because the sum of its digits is divisible by 9.");
                        break;
                    default:
                        break;
                }
            }
        }

        scanner.close();
    }

    private static boolean isDivisible(int number, int divisor) {
        return number % divisor == 0;
    }
}
