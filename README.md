# Program-6-d
## C-Module 6
## EX_NO-06)d)-User Defined datatype
### Date: 19-10-2025
### Name: Anish D
### Register Number:25010086
## AIM:
create a nested structure to read(customer no,name & unit consumption) and store the details of gas customer and calculate the gas bill.
## ALGORITHM:
1. Start the program.
2. Define a structure named gas with three members: 

    a. cno (integer for customer number)  

    b. name (character array of size 20)  

   c. units (integer for units consumed)  
3. Declare a variable of type struct gas.
4. Declare an integer variable amt to store the bill amount and initialize it to 0.
5. Read the customer number, name, and units consumed from the user using scanf.
6. Calculate the bill amount based on the units consumed:
 
    a. If units ≤ 50, amt = units * 10.

    b. If units > 50 and ≤ 100, amt = (50*10) + ((units-50)*20).

    c. If units > 100, amt = (50*10) + (50*20) + ((units-100)*30).
7. Add a fixed charge of 50 to amt.
8. Deduct a 10% discount from amt.
9. Print the final bill amount using printf.
10. End the program.

## PROGRAM:
```
#include<stdio.h>
struct gas
{
    int cno,units;
    char name[20];
};

int main()
{
    int amt=0;
    struct gas g;
    scanf("%d%s%d",&g.cno,g.name,&g.units);
    if(g.units<=50)
    amt=g.units*10;
    else if(g.units<=100&&g.units>50)
    amt=(50*10)+((g.units-50)*20);
    else if(g.units>100)
    amt=(50*10)+(50*20)+((g.units-100)*30);
    amt+=50;
    amt=amt-(amt/10);
    printf("Bill_amount=%d",amt);
    
}
```
## OUTPUT:
<img width="831" height="401" alt="Screenshot 2025-10-20 094529" src="https://github.com/user-attachments/assets/d17416d4-5a76-439c-90a9-7343b03aa42d" />

## RESULT:
Thus the program to read(customer no,name & unit consumption) and store the details of gas customer and calculate the gas bill. has been executed successfully
