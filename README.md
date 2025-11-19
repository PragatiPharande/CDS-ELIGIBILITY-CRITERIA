# CDS-ELIGIBILITY-CRITERIA
C program to check eligibility crieteria of candidates required for CDS exam
c program:


#include <stdio.h>

int main() {
    float marks;
    int age;
   char gender;
   float height;

    printf("Enter your 12th percentage marks: ");
    scanf("%f", &marks);

    if (marks < 60) {
        printf("You are NOT eligible for CDS Exam (marks below 60).\n");
        return 0;
    }

    printf("Enter your age: ");
    scanf("%d", &age);

    if (age < 19 || age > 25) {
        printf("You are NOT eligible for CDS Exam due to age criteria.\n");
    }

printf("Enter your gender (M/F): ");
    scanf(" %c", &gender);

    printf("Enter your height in cm: ");
    scanf("%f", &height);

    if (gender == 'M' || gender == 'm') {
        if (height >= 157) {
            printf("You are eligible to apply for the CDS Exam.\n");
        } else {
            printf("You are NOT eligible due to insufficient height for male candidates.\n");
        }
    }
    else if (gender == 'F' || gender == 'f') {
        if (height >= 152) {
            printf("You are eligible to apply for the CDS Exam.\n");
        } else {
            printf("You are NOT eligible due to insufficient height for female candidates.\n");
        }
    }
    else {
        printf("Invalid gender input.\n");
    }

        return 0;
}

