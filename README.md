# ACD_JAVAB_Session3_Assignment4


import java.util.Scanner;
public class Calculator {
	public void getter(float num1, float num2, char operation) {
		if (operation=='+')
		{
			float sum = num1+num2;
				System.out.println("The sum of two numbers is "+sum);
		}
		else if (operation=='-')
		{
			float diff = num1 - num2;
			System.out.println("The difference of two numbers is "+diff);
		}
		else if (operation=='/')
			{
				float div = num1/num2;
				System.out.println("The division of two numbers is "+div);
			}
		else if (operation=='*')
		{
			float mul = num1*num2;
			System.out.println("The multiplication of two numbers is "+mul);
		}
		else 
			System.out.println("Wrong choice");
		
	}
	public static void main(String args[])
	{
		Calculator calc=new Calculator();
		Scanner number = new Scanner(System.in);
		char choice;
		do
		{
			System.out.println("Enter first Number");
			float num1=number.nextFloat();
			System.out.println("Enter second Number");
			float num2=number.nextFloat();
			System.out.println("Enter operation you want to perform -,+,*,/");
			char operation = number.next(".").charAt(0);
			calc.getter(num1, num2, operation);
			System.out.println("Enter Y  to continue");
			choice = number.next(".").charAt(0);
		}
		while(Character.toLowerCase(choice) == 'y');
		number.close();
	}
}
