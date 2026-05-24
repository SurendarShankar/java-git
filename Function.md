# 04 Function - Method #

## 1.Define two methods to print the maximum and the minimum number respectively among three numbers entered by the user ##

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the value 1 :");
        int a = sc.nextInt();
        System.out.println("Enter the value 2 :");
        int b = sc.nextInt();
        System.out.println("Enter the value 3 :");
        int c = sc.nextInt();

        int large = maximum(a, b, c);
        int small = minimum(a, b, c);

        System.out.println("the max value is : " + large);
        System.out.println("the mim value is : " + small);
        sc.close();
    }

    static int maximum(int a, int b, int c) {
        int max = a;
        if (max < b) {
            max = b;
        }
        if (max < c) {
            max = c;
        }
        return max;
    }

    static int minimum(int a, int b, int c) {
        int min = a;
        if (min > b) {
            min = b;
        }
        if (min > c) {
            min = c;
        }
        return min;
    }
}
```

## 2.Define a program to find out whether a given number is even or odd ##

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner Sc = new Scanner(System.in);
        System.out.print("Enter the number :");
        int value = Sc.nextInt();
        evenorodd(value);
        Sc.close();
    }

    static void evenorodd(int a) {
        if (a % 2 == 0) {
            System.out.println("It is even : " + a);
        } else {
            System.out.println("it is oddd : " + a);
        }
    }
}
```

## 3.A person is eligible to vote if his/her age is greater than or equal to 18. Define a method to find out if he/she is eligible to vote ##

```java
Display
```

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter Your Age : ");
        int age = sc.nextInt();

        eligibility(age);

        sc.close();
    }

    static void eligibility(int a) {

        if (a >= 18) {
            System.out.println("You are eligible for voting");
        } else {
            System.out.println("Oops!");
        }
    }
}
```

```java
Return type 
```

```java
import java.util.Scanner;

public class demo {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter Your age : ");
        int age = sc.nextInt();
        String result = Ebill(age); // changing int to string
        System.out.println(result);
        sc.close();
    }

    static String Ebill(int a) {
        if (a >= 18) {
            return "You can vote " + a;
        } else {
            return "Oops!" + a;
        }
    }
}
```

## Write a program to print the sum of two numbers entered by user by defining your own method ##

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the A value :");
        int a = sc.nextInt();
        System.out.print("Enter the B value :");
        int b = sc.nextInt();
        funSum(a, b);
        sc.close();
    }

    static void funSum(int a, int b) {
        int total = a + b;
        System.out.println("Te sum of two number is : " + total);
    }
}
```

## 5.Write a program to print the sum of two numbers entered by user by defining your own method ##

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the A value :");
        int a = sc.nextInt();
        System.out.print("Enter the B value :");
        int b = sc.nextInt();
        int result = product(a, b);
        System.out.println("The product of 2 num is : " + result);
        sc.close();
    }

    static int product(int a, int b) {
        int total = a * b;
        return total;
    }
}
```

## Math Function chaart ##

| Function        | Purpose        | Example            | Output       |
| ----------------| -------------- | ------------------ | ------------ |
| `Math.abs()`    | Absolute value | `Math.abs(-5)`     | `5`          |
| `Math.max()`    | Largest value  | `Math.max(10,20)`  | `20`         |
| `Math.min()`    | Smallest value | `Math.min(10,20)`  | `10`         |
| `Math.sqrt()`   | Square root    | `Math.sqrt(25)`    | `5.0`        |
| `Math.pow()`    | Power value    | `Math.pow(2,3)`    | `8.0`        |
| `Math.round()`  | Round value    | `Math.round(12.6)` | `13`         |
| `Math.ceil()`   | Round up       | `Math.ceil(12.1)`  | `13.0`       |
| `Math.floor()`  | Round down     | `Math.floor(12.9)` | `12.0`       |
| `Math.random()` | Random number  | `Math.random()`    | `0.0 to 1.0` |

## 6.Write a program to print the circumference and area of a circle of radius entered by user by defining your own method ##

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the Radius :");
        double radius = sc.nextDouble();
        curcumference(radius);
        area(radius);
        sc.close();
    }

    static void curcumference(double r) {
        Double circum = 2 * 3.14 * r;
        System.out.println("Curcumference of Circle is :" + Math.round(circum));
    }

    static void area(double r) {
        double arearvalue = 3.14 * r * r;
        System.out.println("The Area of Circle is : " + arearvalue);
    }
}
```

## 7.Define a method to find out if a number is prime or not ##

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the Number : ");
        int num = sc.nextInt();

        primenumber(num);

        sc.close();
    }

    static void primenumber(int n) {

        boolean isPrime = true;

        if (n <= 1) {
            isPrime = false;
        }
        else {

            for (int i = 2; i <= n - 1; i++) {

                if (n % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }

        if (isPrime) {
            System.out.println("It is a Prime Number : " + n);
        }
        else {
            System.out.println("It is Not a Prime Number : " + n);
        }
    }
}
```

## 8.Write a program that will ask the user to enter his/her marks (out of 100). Define a method that will display grades according to the marks entered as below ##

```java
Marks        Grade 
91-100         AA 
81-90          AB 
71-80          BB 
61-70          BC 
51-60          CD 
41-50          DD 
<=40          Fail 
```

```java
import java.nio.channels.Pipe.SourceChannel;
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter Your Mark : ");
        int mark = sc.nextInt();
        grade(mark);
        sc.close();
    }

    static void grade(int m) {
        if (m >= 91 && m <= 100) {
            System.out.println("Your Grade is : " + "AA");
        }
        else if (m >= 81 && m <= 90) {
            System.out.println("Your Grade is : " + "AB");
        }
        else if (m >= 71 && m <= 80) {
            System.out.println("Your Grade is : " + "BB");
        }
        else if (m >= 61 && m <= 70) {
            System.out.println("Your Grade is : " + "BC");
        }
        else if (m >= 51 && m <= 60) {
            System.out.println("Your Grade is : " + "CD");
        }
        else if (m >= 41 && m <= 50) {
            System.out.println("Your Grade is : " + "DD");
        } 
        else {
            System.out.println("You are Fail ! | Try Again !!");
        }
    }
}
```
