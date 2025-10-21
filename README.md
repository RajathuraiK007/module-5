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
#include<stdio.h>
int main()
{
    float a,b;
    float *pa=&a,*pb=&b;
    scanf("%f %f",pa,pb);
    float area=(*pa)*(*pb);
    printf("Area of the triangle is %.2f",area);
    return 0;
}

## OUTPUT
<img width="1616" height="468" alt="image" src="https://github.com/user-attachments/assets/07d74d54-317d-4b76-878a-8b47d1e5421b" />


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
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main()
{
    char*str=(char*)malloc(8*sizeof(char));
    strcpy(str,"WELCOME");
    printf("%s",str);
    free(str);
    return 0;
}

## OUTPUT
<img width="1748" height="399" alt="image" src="https://github.com/user-attachments/assets/72f8a0df-bd6b-4488-bc5d-5aabad16a943" />



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
#include<stdio.h>
struct
{
    char Name[15];
    int roll_no;
    int marks;
}s1;
int main()
{
    scanf("%s %d %d",s1.Name,&s1.roll_no,&s1.marks);
    printf("Student name:%s\nRoll.No:%d\nMarks Scored:%d",s1.Name,s1.roll_no,s1.marks);
    return 0;
}

## OUTPUT
<img width="1629" height="524" alt="image" src="https://github.com/user-attachments/assets/d6239db8-3321-451e-826d-29b444cc49e9" />


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
#include<stdio.h>
struct Employee
{
    char Name[15];
    int id;
    float BasicSal;
    float HRA;
    float DA;
};
int main()
{
    struct Employee e[3];
    for(int i=0;i<3;i++)
    {
        scanf("%s %d %f %f %f",e[i].Name,&e[i].id,&e[i].BasicSal,&e[i].HRA,&e[i].DA);
    }
    for(int i=0;i<3;i++)
    {
        float Gross=e[i].BasicSal+e[i].HRA+e[i].DA;
        printf("Employee name: %s\nEmployee ID: %d\nGross salary: %.2f\n\n",e[i].Name,e[i].id,Gross);
    }
    return 0;
}

 ## OUTPUT
<img width="1799" height="745" alt="image" src="https://github.com/user-attachments/assets/6ab758e7-be89-4587-8a7a-44235b4ffa12" />

 

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
#include<stdio.h>
struct Employee
{
    char Name[15];
    int Roll_no;
    int Subject[5];
    int Total;
}s[2];
int main()
{
   
for(int i=0;i<2;i++)
{
      scanf("%d\n",&s[i].Roll_no); 
    for(int j=0;j<5;j++)
    {
      
        scanf("%d",&s[i].Subject[j]);
    }
}
    for(int i=0;i<2;i++)
    {
        s[i].Total=0;
    }
    for(int i=0;i<2;i++)
    {
    for(int j=0;j<5;j++)
    {
        s[i].Total+=s[i].Subject[j];
    }
    }
for(int i=0;i<2;i++)
{
    printf("Total(%d) = %d\n",s[i].Roll_no,s[i].Total);
}
    return 0;
}

## OUTPUT

<img width="1519" height="739" alt="image" src="https://github.com/user-attachments/assets/ebb76cf7-e9cd-454e-9722-ce50623ea0c3" />

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


