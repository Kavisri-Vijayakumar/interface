package calculatorprogram;
import java.util.Scanner;
interface calculator{
    double add (double a, double b);

    double subtract(double a, double b);
    double multiply(double a, double b);
    double divide(double a, double b);
}
class simplecalculator implements calculator {
@Override
public double add(double a,double b){
return a+b;
}
@Override
public double subtract(double a,double b){
return a-b;
}
@Override
public double multiply(double a, double b){
return a*b;
}
@Override
public double divide(double a,double b) {
    if(b==0){
        System.out.println("error:division by zero not allowed!");
        return Double.NaN;
    }
    return a/b;
}       
    }
public class Calculatorprogram {
    public static void main(String[] args) {
        Scanner scanner=new Scanner(System.in);
        calculator Calculator =new simplecalculator();
        System.out.println("welcome to the simple calculator!");
        System.out.println("enter the first number:");
        double num1=scanner.nextDouble();
        System.out.println("enter the second number:");
        double num2=scanner.nextDouble();
        System.out.println("\nresults:");
        System.out.println("addition:"+Calculator.add(num1,num2));
        System.out.println("subtraction:"+Calculator.subtract(num1,num2));
        System.out.println("multiplication:"+Calculator.multiply(num1,num2));
        System.out.println("division:"+Calculator.divide(num1,num2));
        scanner.close();
        
    }
    
}
output

