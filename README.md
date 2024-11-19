# Destructor-Static-variable-class-method             
using System;
public static class BankUtilities {

// Static variable shared by all methods
public static double InterestRate = 0.05; // 5% interest rate by default

// Static method to calculate interest based on balance

public static double CalculateInterest(double balance) {

return balance * InterestRate;

}
// Static method to update the interest rate for the entire class
public static void UpdateInterestRate(double newRate) {
InterestRate = newRate;
Console.WriteLine("Interest rate updated to: " + (InterestRate * 100) + "%");

 }
}

class Program {

static void Main() {

// Using the static variable and method without creating an instance

Console.WriteLine("Default Interest Rate: " + (BankUtilities.InterestRate * 100) + "%");

double balance = 1000;

double interest = BankUtilities.CalculateInterest(balance);

Console.WriteLine("Interest on balance $" + balance + " is: $" + interest);

// Updating the interest rate using static method

BankUtilities.UpdateInterestRate(0.07); // Updating to 7%

// Recalculating interest with the new rate

interest = BankUtilities.CalculateInterest(balance);

Console.WriteLine("New interest on balance $" + balance + " is: $" + interest);

}

}
