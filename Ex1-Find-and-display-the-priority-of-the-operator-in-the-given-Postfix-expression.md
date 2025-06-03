# EX 1 Display operator precedence in the infix expression.
## DATE: 23/05/2025
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1. Read the postfix expression as a string input.

2. Loop through each character of the postfix expression one by one.

3. For each character, check if it is an operator (i.e., not an alphanumeric character).

4. If it is an operator, determine its priority using the priority function.

5. Print the operator along with its priority.

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Thanika Sree b
RegisterNumber: 212222100055 
*/

#include <stdio.h>
#include <ctype.h>

int priority(char x) {
    if (x == '|') return 1;
    if (x == '&') return 2;
    if (x == '+' || x == '-') return 3;
    if (x == '*' || x == '/' || x == '%') return 4;
    if (x == '^') return 5;
    return 0;
}

int main() {
    char exp[100];
    printf("Enter postfix expression: ");
    scanf("%s", exp);

    for (int i = 0; exp[i] != '\0'; i++) {
        if (!isalnum(exp[i])) {  // if operator
            printf("Operator: %c, Priority: %d\n", exp[i], priority(exp[i]));
        }
    }

    return 0;
}
```

## Output:

![image](https://github.com/user-attachments/assets/5c481280-bfe1-41b7-942b-e67a8335a673)


## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
