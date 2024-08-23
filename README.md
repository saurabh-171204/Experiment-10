# Experiment-10
## AIM
To study and implement Pointer Operations (Call by value and Call by reference).
## THEORY
Pointers are symbolic representations of addresses.
We can pass arguments to funtions using different methods mainly call by value and call by reference.

### Call by value
In the call-by-value method, function arguments are passed by copying the value of the actual parameter, ensuring the original values remain unchanged.
The value is copied to the formal parameter.
Any changes made to the parameters within the function do not change the original values outside the function.

### Call by reference
In the call-by-reference method, the memory address (reference) of the actual parameter is passed to the function, allowing direct access and modification of the original values.
The actual and the formal parameters point to the same memory address.

Any changes made to the parameters within the function are directly reflected in the original values outside the function.
## CODE AND OUTPUT
A
```
// Printing the values by using callby value 

#include<iostream> 
using namespace std; 
void swap(int x, int y) 
{
    int swap;
    swap=x;
    x=y;
    y=swap;
}

int main() 
{
    int a=4, b=7;
    swap(a,b);
    cout<<"Value of a is: "<<a<<"\n";
    cout<<"Value of b is: "<<b<<"\n";
    return 0;
}
```
![Output_10A](https://github.com/user-attachments/assets/e4d4ca93-8caa-4a4c-8c7a-562335b08f1f)

B
```// Swapping the values 

#include<iostream> 
using namespace std; 
void swap(int *x, int *y) 
{
    int *swap;
    swap=x;
    x=y;
    y=swap;
}

int main() 
{
    int a=4,b=7;
    swap(a,b);
    cout<<"Value of a is: "<<a<<"\n";
    cout<<"Value of b is: "<<b<<"\n";
    return 0;
}
```
![Output_10B](https://github.com/user-attachments/assets/c7d63862-3955-4884-95a8-eda93f2ba60d)

C
```
// Swapping the values using call by reference  

#include<iostream> 
using namespace std; 
void swap(int *x, int *y) 
{
    int swap;
    swap=*x;
    *x=*y;
    *y=swap;
}

int main() 
{
    int a=4,b=7;
    swap(&a,&b);
    cout<<"Value of a is: "<<a<<"\n";
    cout<<"Value of b is: "<<b<<"\n";
    return 0;
}
```
![Output_10C ](https://github.com/user-attachments/assets/a6c2af15-d112-4703-80f3-8e5ca87179fe)
## CONCLUSION
I learnt about pointers and how to pass arguments to functions using call by value and call by reference methods. I also learnt how to swap values using call by reference.
