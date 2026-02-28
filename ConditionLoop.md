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

## 4.Calculate Discount Of Product

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the Market Price :");
        int mp = sc.nextInt();
        System.out.print("Enter the Discount :");
        int D = sc.nextInt();

        // Calculate the Discount
        int Discount = ((mp * D) / 100);
        System.out.println("Discount Amount is:" + Discount);

        // Selling price
        int sp = mp - Discount;
        System.out.println("The Selling price :" + sp);
        sc.close();

    }
}
```

## 5.Calculate Distance Between Two Points

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the value X1 and x2 :");
        double x1 = sc.nextDouble();
        double x2 = sc.nextDouble();
        System.out.println("Enter the value Y1 and Y2 :");
        double y1 = sc.nextDouble();
        double y2 = sc.nextDouble();

        // sub
        double x = (x1 - x2);
        double y = (y1 - y2);

        // squar
        double SquarX = Math.pow(x, 2);
        double SquarY = Math.pow(y, 2);

        // Squar valu is add

        // double addvalue = SquarX + SquarY;
        double result = Math.sqrt(SquarX + SquarY);
        System.out.println("The distance between 2 point is:" + result);
        sc.close();

    }
}
```

## 6.Calculate Commission Percentage

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Commission earned :");
        double ce = sc.nextDouble();
        System.out.print("Sales amount  :");
        double sa = sc.nextDouble();
        double result = ((ce / sa) * 100);

        System.out.println("the % is :" + result + "%");
        sc.close();

    }
}
```
