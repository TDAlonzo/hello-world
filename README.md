# hello-world
import java.util.Scanner;

public class HelloWorld 
{
	
static double initialBalance = 15000;
static double payment;
static double newBalance;
static double rentDue;

	public static void main(String[] args) 
	{
		Scanner in = new Scanner(System.in);
		System.out.println("----------------------------------------------------------------");
		System.out.println("This system will determine if you still need to pay rent.");
		System.out.println("Please enter how much you have paid this month and we will");
		System.out.println("determine if you need to pay anything additional");
		System.out.println("----------------------------------------------------------------");
		int input = in.nextInt();
		rent(input);
	}
	
	public static double rent (double rentDue)
	{
		if (rentDue <= 850)
		{
			payment = 850 - rentDue;
			System.out.println("You need to pay an additional $" +payment +" this month");
			newBalance = initialBalance - payment;
			System.out.println("Your new Balance after payment is: $" +newBalance);
		}
		else
		{
			payment = 0;
			System.out.println("You do not need to make a payment at this time.");
			System.out.println("Your current Balance is: $" +initialBalance);
		}
		return newBalance;
	}	
}
