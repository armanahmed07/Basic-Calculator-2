#include <stdio.h>
#include <string.h> 

int main() {
    float num1, num2, result;
    char op;
    char choice[10]; 

    do {
        printf("Enter first number: ");
        scanf("%f", &num1);
        printf("Enter second number: ");
        scanf("%f", &num2);
        printf("Choose operation (+, -, *, /): ");
        scanf(" %c", &op);

        switch (op) {
            case '+':
                result = num1 + num2;
                printf("Result: %.2f + %.2f = %.2f\n", num1, num2, result);
                break;
            case '-':
                result = num1 - num2;
                printf("Result: %.2f - %.2f = %.2f\n", num1, num2, result);
                break;
            case '*':
                result = num1 * num2;
                printf("Result: %.2f * %.2f = %.2f\n", num1, num2, result);
                break;
            case '/':
                if (num2 == 0)
                    printf("Error: Division by zero!\n");
                else {
                    result = num1 / num2;
                    printf("Result: %.2f / %.2f = %.2f\n", num1, num2, result);
                }
                break;
            default:
                printf("Invalid operation!\n");
        }

        printf("Continue? (yes/no): ");
        scanf("%s", choice);
    } while (strcmp(choice, "yes") == 0 || strcmp(choice, "Yes") == 0);

    return 0;
}
