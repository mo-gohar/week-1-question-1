//week-1-question-1
#include <stdio.h>

int main() {
    int num, i, isPerfectSquare;

    do {
        printf("Enter a positive integer: ");
        scanf("%d", &num);

        if (num <= 0) {
            printf("Invalid input! Please enter a positive integer.\n");
            continue;
        }

        isPerfectSquare = 0;

        for (i = 1; i * i <= num; i++) {
            if (i * i == num) {
                isPerfectSquare = 1;
                break;
            }
        }

        if (!isPerfectSquare)
            printf("%d is not a perfect square. Try again!\n", num);

    } while (!isPerfectSquare);

    printf("%d is a perfect square!\n", num);

    return 0;
}
