# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
  
    float length, width, area;
    float *ptrLength = &length;
    float *ptrWidth = &width;

   
    printf("Enter the length of the rectangle: ");
    scanf("%f", ptrLength);
    printf("Enter the width of the rectangle: ");
    scanf("%f", ptrWidth);

   
    area = (*ptrLength) * (*ptrWidth);

 
    printf("Area of the rectangle is: %.2f\n", area);

   
    return 0;
}
```

## OUTPUT
		       	
<img width="454" height="190" alt="Screenshot 2025-10-19 212012" src="https://github.com/user-attachments/assets/415835ed-0c90-4161-958c-ea7c0f01d6d9" />


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    char *str;

   
    str = (char *)malloc(8 * sizeof(char)); 
    if (str == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }

   
    strcpy(str, "WELCOME");

   
    printf("%s\n", str);

   
    free(str);

   
    return 0;
}
```

## OUTPUT

<img width="505" height="136" alt="Screenshot 2025-10-19 212159" src="https://github.com/user-attachments/assets/5fd6ea60-34d7-4a47-bc26-1c4af872a13f" />


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 




# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

// Step 2: Create a structure for student
struct Student {
    char name[50];
    int rollNo;
    float marks;
};

int main() {
    
    struct Student student;

   
    printf("Enter student's name: ");
    scanf(" %[^\n]s", student.name); 
    printf("Enter student's roll number: ");
    scanf("%d", &student.rollNo);
    printf("Enter student's marks: ");
    scanf("%f", &student.marks);

    
    printf("\nStudent Information:\n");
    printf("Name      : %s\n", student.name);
    printf("Roll No   : %d\n", student.rollNo);
    printf("Marks     : %.2f\n", student.marks);

    
    return 0;
}
```



## OUTPUT

<img width="511" height="307" alt="Screenshot 2025-10-19 212506" src="https://github.com/user-attachments/assets/652f8f74-eb98-4c01-9927-0a0e21f2099d" />


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <string.h>

// Define a structure for employee
struct Employee {
    char name[50];
    int id;
    float basicSalary;
    float hra;      // House Rent Allowance
    float da;       // Dearness Allowance
    float grossSalary;
};

int main() {
    struct Employee emp[3];
    int i;

    
    for(i = 0; i < 3; i++) {
        printf("Enter details for Employee %d:\n", i + 1);

        printf("Name: ");
        scanf(" %[^\n]s", emp[i].name);

        printf("ID: ");
        scanf("%d", &emp[i].id);

        printf("Basic Salary: ");
        scanf("%f", &emp[i].basicSalary);

        printf("HRA: ");
        scanf("%f", &emp[i].hra);

        printf("DA: ");
        scanf("%f", &emp[i].da);

        // Calculate Gross Salary
        emp[i].grossSalary = emp[i].basicSalary + emp[i].hra + emp[i].da;

        printf("\n");
    }

    // Print employee details with gross salary
    printf("Employee Details and Gross Salary:\n");
    printf("---------------------------------------------------\n");
    printf("Name\tID\tBasic\tHRA\tDA\tGross Salary\n");
    printf("---------------------------------------------------\n");

    for(i = 0; i < 3; i++) {
        printf("%s\t%d\t%.2f\t%.2f\t%.2f\t%.2f\n", 
               emp[i].name, emp[i].id, emp[i].basicSalary, emp[i].hra, emp[i].da, emp[i].grossSalary);
    }

    return 0;
}
```



 ## OUTPUT

 <img width="851" height="701" alt="Screenshot 2025-10-19 212957" src="https://github.com/user-attachments/assets/e9bccbcd-335d-4c53-8856-bbe39def02a2" />


## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

// Define a structure for student
struct Student {
    char name[10];     // Student's name (optional)
    int rollno;        // Roll number (optional)
    int subject[5];    // Marks of 5 subjects
    int total;         // Total marks
    float average;     // Average marks
};

int main() {
    struct Student s[2]; 
    int i, j;

    // Input marks for each student
    for(i = 0; i < 2; i++) {
        printf("Enter details for Student %d:\n", i + 1);

        printf("Name: ");
        scanf("%s", s[i].name);

        printf("Roll No: ");
        scanf("%d", &s[i].rollno);

        s[i].total = 0; 

        printf("Enter marks for 5 subjects: ");
        for(j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
            s[i].total += s[i].subject[j]; 
        }

        // Calculate average
        s[i].average = s[i].total / 5.0;

        printf("\n");
    }

    // Display total and average for each student
    printf("Student Details with Total and Average Marks:\n");
    printf("-------------------------------------------------\n");
    printf("Name\tRollNo\tTotal\tAverage\n");
    printf("-------------------------------------------------\n");

    for(i = 0; i < 2; i++) {
        printf("%s\t%d\t%d\t%.2f\n", s[i].name, s[i].rollno, s[i].total, s[i].average);
    }

    return 0;
}
```


## OUTPUT

 <img width="639" height="485" alt="Screenshot 2025-10-19 213244" src="https://github.com/user-attachments/assets/e953ac2c-dfb2-4867-9d3c-0ec57f1f5383" />


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


