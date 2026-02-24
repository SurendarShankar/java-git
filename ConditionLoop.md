# Intermediate Java Programs

## 1.Factorial Program In Java

```java
import java.util.Scanner;
public class hello {
    public static void main(String[] args) {
        Scanner sc = new  Scanner(System.in);
        System.out.print("Enter the Number :");
         int value = sc.nextInt();
         int result = 1;
         

         for(int i = 1 ;i<=value;i++)
         {
            result = result*i;
            System.out.println(result);
            
         }
         System.out.println("the Total value is : " + result );
         sc.close();
    }
}
```

### Using function

```java
public class demo {

    static long factorial(int n) {
        if (n == 0 || n == 1)
            return 1;
        return n * factorial(n - 1);
    }

    public static void main(String[] args) {
        int num = 5;
        System.out.println("Factorial = " + factorial(num));
    }
}
```

## 2.Calculate Electricity Bill

```java
import java.util.Scanner;

public class ElectricityBill {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter units consumed: ");
        int units = sc.nextInt();

        double bill = 0;

        if (units <= 100) {
            bill = units * 1.50;
        } 
        else if (units <= 200) {
            bill = (100 * 1.50) + ((units - 100) * 2.50);
        } 
        else if (units <= 300) {
            bill = (100 * 1.50) + (100 * 2.50) + ((units - 200) * 4.00);
        } 
        else {
            bill = (100 * 1.50) + (100 * 2.50) + (100 * 4.00) + ((units - 300) * 6.00);
        }

        System.out.println("Electricity Bill = ₹" + bill);

        sc.close();
    }
}
```
