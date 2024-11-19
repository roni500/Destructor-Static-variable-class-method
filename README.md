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
