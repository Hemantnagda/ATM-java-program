import java.util.Scanner;
public class ATMdemo {
     static double balance = 10000;
    static Scanner sc = new Scanner(System.in);
    public static void main(String[] args) {
         int choice;
      System.out.println("Welcome to ATM Machine");
      do {
            System.out.println("\n------ ATM Menu ------");
            System.out.println("1. Check Balance");
            System.out.println("2. Deposit Money");
            System.out.println("3. Withdraw Money");
            System.out.println("4. Exit");
            System.out.print("Enter your choice: ");
            choice = sc.nextInt();
            switch (choice) {
                case 1:
                checkbalance ();
                    break;

                case 2:
                    depositMoney();
                    break;

                case 3:
                    withdrawMoney();
                    break;

                case 4:
                    System.out.println("Thank you for using ATM");
                    break;

                default:
                    System.out.println("Invalid choice! Please try again.");
            }

        } while (choice != 4);
    }

    private static void checkbalance() {
           }
    public static void checkBalance() {
        System.out.println("Your current balance is: ₹" + balance);
    }

    public static void depositMoney() {
        System.out.print("Enter amount to deposit: ");
        double amount = sc.nextDouble();

        if (amount > 0) {
            balance = balance + amount;
            System.out.println("Money deposited successfully.");
            System.out.println("Updated Balance: ₹" + balance);
        } else {
            System.out.println("Invalid deposit amount!");
        }
    }

    public static void withdrawMoney() {
        System.out.print("Enter amount to withdraw: ");
        double amount = sc.nextDouble();

        if (amount > 0 && amount <= balance) {
            balance = balance - amount;
            System.out.println("Please collect your cash.");
            System.out.println("Remaining Balance "+" balance");
        } else {
            System.out.println("Invalid or insufficient balance!");
        }
    }
}

