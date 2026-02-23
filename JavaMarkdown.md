# FUNDAMENTAL LOGIC PROBLEMS  

## 1.Input a year and find whether it is a leap year or not

```java
import java.util.Scanner;
public class hello {

    public static void main(String[] args) {
        System.out.print("Enter the year : ");
        Scanner input  = new Scanner(System.in);
        int a = input.nextInt();

        if (a%400==0) {
            System.out.println("It is a leap Year");
        }
        else if (a%100==0) {
            System.out.println("It is not a leap Year");
        }
        else if (a%4==0) {
            System.out.println("It is a leap Year");
        }
        else{
            System.out.println("It is not leap Year");
        }
        input.close();
    }
}
```

### 2.Take 2 numbers as inputs and find their HCF and LCM

```java
import java.util.Scanner;
public class hello {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the number :");
        int a = sc.nextInt();
        int b = sc.nextInt();

        int count = 0;

        /*
        for(int i=1;i<=b;i++)
         */
        
        int i = 1;
        while (i<=a) {
            if (a%i==0 && b%i==0) {
               count = i; 
            }
            i++;
        }
        System.out.println(count);

        int lcm = a*b/count;
        {
            System.out.println(lcm);
        }
        sc.close();
    }
}
```

## 3.Keep taking numbers as inputs till the user enters ‘x’, after that print sum of all

```java
import java.util.Scanner;
public class hello {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int sum = 0;

        while (true) {
            System.out.print("Enter the num (or) 'x' to print the total Sum : " );
            char ch = input.next().trim().charAt(0);

            if (ch == 'x'|| ch == 'X' ) {
                break;
            }
            else{
                //converting  char to int // //1.ch to string  2.string to num
               int value = Integer.parseInt(String.valueOf(ch)); 
               //int value = (ch) - '0'; // direct method for ch to int :
               sum  = sum + value ;
            }    
        }
        System.out.println( "the total Sum is : " + sum);
        input.close();
    }
}
```

## 4.Take name as input and print a greeting message for that particular name

```java
import java.util.Scanner;
public class demo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the Name :");
        String name = sc.nextLine();
        System.out.println("hi !" + name  +" I Love You ");
        sc.close();

    }
}
```

## 5.Write a program to input principal, time, and rate (P, T, R) from the user and find Simple Interest

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the Principle :");
        int p = sc.nextInt();
        System.out.print("Enter the year :");
        int t = sc.nextInt();
        System.out.print("Enter the Rate of intrest :");
        int r = sc.nextInt();
        int result = ( (p*t*r)/100 ) ;
        System.out.println(result);
        sc.close();
    }
}
```

## 6.Take in two numbers and an operator (+, -, *, /) and calculate the value. (Use if conditions)

**If else :**

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the N1 value : ");
        int n1 = sc.nextInt();
        System.out.print("Enter the N2 value : ");
        int n2 = sc.nextInt();
        System.out.print("Enter the Operator : ");
        char op = sc.next().trim().charAt(0);

        if (op == '+') {
            System.out.println(n1 + n2);
        } else if (op == '-') {
            System.out.println(n1 - n2);
        } else if (op == '*') {
            System.out.println(n1 * n2);
        } else if (op == '/') {
            System.out.println(n1 / n2);
        } else {
            System.out.println("No operator is entered !");
        }
        sc.close();

    }
}
```

**Switch :**

```java
System.out.print("Enter first number: ");
int num1 = sc.nextInt();

System.out.print("Enter operator: ");
char op = sc.next().charAt(0);

System.out.print("Enter second number: ");
int num2 = sc.nextInt();

switch(op) {
    case '+':
        System.out.println(num1 + num2);
        break;
    case '-':
        System.out.println(num1 - num2);
        break;
    case '*':
        System.out.println(num1 * num2);
        break;
    case '/':
        System.out.println(num1 / num2);
        break;
    default:
        System.out.println("Invalid operator");
}
```

## 7.Input currency in rupees and output in USD

```java
import java.util.Scanner;

public class hello {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the value in RS : ");
        int Rs = sc.nextInt();

        int result = (Rs/83);
        System.out.println("The USD value of RS is  : " + result);
        sc.close();


    }
}
```
