Write a C program to find the maximum of three numbers without using logical operators.

AIM:

To Write a C program to find the maximum of three numbers without using logical operators.

Algorithm:
```
1.Start
2.Input three numbers: a, b, c
3.Assume a is the maximum → max = a
4.Compare b with max
    If b > max, then assign max = b
5.Compare c with max
    If c > max, then assign max = c
6.Display max
7.Stop
```
Program:
```
#include <stdio.h>

int main() {
    int a, b, c, max;

    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);

    max = a;

    if (b > max) {
        max = b;
    }

    if (c > max) {
        max = c;
    }

    printf("Maximum = %d\n", max);

    return 0;
}

```

Output:

<img width="1920" height="1200" alt="Screenshot (764)" src="https://github.com/user-attachments/assets/cbfd8782-9f51-4165-9389-fef183722efe" />

Result:

Thus the execution of C program to find the maximum of three numbers without using logical operators.

2.Write a  C program to check whether the given year is leap year or not by adding century leap year or non-century leap year in the output (Eg: 2000 is a century leap year, 2024 is a non-century leap year)


AIM:

To Write a  C program to check whether the given year is leap year or not by adding century leap year or non-century leap year in the output (Eg: 2000 is a century leap year, 2024 is a non-century leap year)

Algorithm:
```
1.Start

2.Input the year y

3.If y % 400 == 0

   Then it is a century leap year

4.Else if y % 100 == 0

   Then it is not a leap year

5.Else if y % 4 == 0

   Then it is a non-century leap year

6.Else

   It is not a leap year

7.Display the result

8.Stop
```

Program:
```
#include <stdio.h>

int main() {
    int year;

    printf("Enter a year: ");
    scanf("%d", &year);

    if (year % 400 == 0) {
        printf("%d is a century leap year\n", year);
    }
    else if (year % 100 == 0) {
        printf("%d is not a leap year\n", year);
    }
    else if (year % 4 == 0) {
        printf("%d is a non-century leap year\n", year);
    }
    else {
        printf("%d is not a leap year\n", year);
    }

    return 0;
}
```

Output:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/19c0cc96-76aa-41db-b047-ab1ab4efa5d8" />

Result:

Thus the executioin of C program to check whether the given year is leap year or not by adding century leap year or non-century leap year in the output (Eg: 2000 is a century leap year, 2024 is a non-century leap year)

3.Write a C program to find whether the entered character is alphabet / digit / special character. If the entered character is an alphabet then say it is vowel or consonant without using built in functions.

AIM:

To write a C program to find whether the entered character is alphabet / digit / special character. If the entered character is an alphabet then say it is vowel or consonant without using built in functions.

Algorithm:
```
1.Start
2.Input a character ch
3.Check if ch is an alphabet:
4.If (ch is between 'A' to 'Z' OR 'a' to 'z')
    Then it is an alphabet
5.Check if it is a vowel:
6.If ch is 'A', 'E', 'I', 'O', 'U' or 'a', 'e', 'i', 'o', 'u'
→ It is a vowel
7.Else → It is a consonant
8.Else if (ch is between '0' to '9')
9.Then it is a digit
   Else
10.It is a special character
11.Display the result
12.Stop
```
Program:
```
#include <stdio.h>

int main() {
    char ch;

    printf("Enter a character: ");
    scanf(" %c", &ch);

    // Check if alphabet
    if ((ch >= 'A' && ch <= 'Z') || (ch >= 'a' && ch <= 'z')) {
        printf("It is an alphabet\n");

        // Check vowel or consonant
        if (ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U' ||
            ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
            printf("It is a vowel\n");
        } else {
            printf("It is a consonant\n");
        }
    }
    // Check if digit
    else if (ch >= '0' && ch <= '9') {
        printf("It is a digit\n");
    }
    // Otherwise special character
    else {
        printf("It is a special character\n");
    }

    return 0;
}


```

Output:

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/5a7ed8f3-f8bb-47d1-be8e-4749c5f55e16" />

Result:

Thus the Execution of C program to find whether the entered character is alphabet / digit / special character. If the entered character is an alphabet then say it is vowel or consonant without using built in functions.

4.Write a  C program for simple ATM simulation with operations Check Balance, Deposit,  Withdraw,  Exit using switch and update balance accordingly.

AIM:

To Write a  C program for simple ATM simulation with operations Check Balance, Deposit,  Withdraw,  Exit using switch and update balance accordingly.

Algorithm:
```
1.Start
2.Initialize balance (e.g., balance = 1000)
3.Repeat until user chooses Exit:
    Display menu:
    Check Balance
    Deposit
    Withdraw
    Exit
3.Read user choice
    Use switch:
    Case 1: Display balance
    Case 2: Input deposit amount and add to balance
    Case 3: Input withdraw amount
4.If amount ≤ balance → subtract from balance
5.Else → show “Insufficient balance”
     Case 4: Exit program
     Default: Invalid choice
6.Stop
```
Program:
```
#include <stdio.h>

int main() {
    int choice;
    float balance = 1000.0, amount;

    do {
        printf("\n--- ATM MENU ---\n");
        printf("1. Check Balance\n");
        printf("2. Deposit\n");
        printf("3. Withdraw\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Current Balance: %.2f\n", balance);
                break;

            case 2:
                printf("Enter amount to deposit: ");
                scanf("%f", &amount);
                if (amount > 0) {
                    balance = balance + amount;
                    printf("Amount deposited successfully\n");
                } else {
                    printf("Invalid amount\n");
                }
                break;

            case 3:
                printf("Enter amount to withdraw: ");
                scanf("%f", &amount);
                if (amount <= balance && amount > 0) {
                    balance = balance - amount;
                    printf("Withdrawal successful\n");
                } else {
                    printf("Insufficient balance or invalid amount\n");
                }
                break;

            case 4:
                printf("Thank you! Exiting...\n");
                break;

            default:
                printf("Invalid choice\n");
        }

    } while (choice != 4);

    return 0;
}

```
Output:

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/5305bc50-552a-4735-9071-8175fe1922d9" />

Result:

Thus the execution of C program for simple ATM simulation with operations Check Balance, Deposit,  Withdraw,  Exit using switch and update balance accordingly.

5.Write a C program for menu driven calculator using switch statement.

AIM;

To Write a C program for menu driven calculator using switch statement.

Algorithm:
```
1.Start
    Display menu:
    Addition
    Subtraction
    Multiplication
    Division
    Exit
2.Input user choice
    If choice is between 1–4:
    Input two numbers (a, b)
3.Use switch:
    Case 1 → result = a + b
    Case 2 → result = a - b
    Case 3 → result = a * b
    Case 4 →
4.If b != 0 → result = a / b
   Else → print error (division by zero)
5.Case 5 → Exit
    Default → Invalid choice
6.Display result
7.Repeat until Exit
8.Stop
```
Program:
```
#include <stdio.h>

int main() {
    int choice;
    float a, b, result;

    do {
        printf("\n--- CALCULATOR MENU ---\n");
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Exit\n");

        printf("Enter your choice: ");
        scanf("%d", &choice);

        if (choice >= 1 && choice <= 4) {
            printf("Enter two numbers: ");
            scanf("%f %f", &a, &b);
        }

        switch (choice) {
            case 1:
                result = a + b;
                printf("Result = %.2f\n", result);
                break;

            case 2:
                result = a - b;
                printf("Result = %.2f\n", result);
                break;

            case 3:
                result = a * b;
                printf("Result = %.2f\n", result);
                break;

            case 4:
                if (b != 0) {
                    result = a / b;
                    printf("Result = %.2f\n", result);
                } else {
                    printf("Error: Division by zero\n");
                }
                break;

            case 5:
                printf("Exiting calculator...\n");
                break;

            default:
                printf("Invalid choice\n");
        }

    } while (choice != 5);

    return 0;
}

```
Output;

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/98ec59ab-2a9e-4f3b-9c74-edeeef28b99f" />

Result;

Thus the Execution of  a C program to find the maximum of three numbers without using logical operators.
