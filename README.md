# C++
pointers 


// Online C++ compiler to run C++ program online
#include <stdio.h>

// Function that takes an int and returns its square
int square(int x) {
    return x * x;
}

int main() {
    int num = 5;

    // 1. Call the function normally
    int result1 = square(num);
    printf("Normal call: %d squared = %d\n", num, result1);

    // 2. Call the function using a function pointer
    int (*func_ptr)(int) = square;  // Declare a function pointer and assign it
    int result2 = func_ptr(num);     // Call the function through the pointer
    printf("Function pointer call: %d squared = %d\n", num, result2);

    return 0;
}



#include <stdio.h>

int main() {
    int a = 10;      // Declare a variable 'a' and assign 10
    int *ptr = &a;   // Declare a pointer 'ptr' and store the address of 'a'

    // 1. Print the value of the variable
    printf("Value of a: %d\n", a);

    // 2. Print the address of the variable
    printf("Address of a: %p\n", (void*)&a);

    // 3. Print the value stored in the pointer (which is the address of 'a')
    printf("Value stored in pointer ptr: %p\n", (void*)ptr);

    // Optional: Print the value pointed to by the pointer
    printf("Value pointed to by ptr: %d\n", *ptr);

    return 0;
}


#include <stdio.h>

int main() {
    int a = 10;  // Create a variable 'a' and give it the value 10

    // Print the value of the variable
    printf("Value of a: %d\n", a);

    return 0;
}


#include <stdio.h>

int main() {
    int a = 10;  // Variable

    // Print the address of the variable
    printf("Address of a: %p\n", (void*)&a);

    return 0;
}

#include <stdio.h>

int main() {
    int a = 10;       // A variable
    int *ptr = &a;    // Pointer stores the address of 'a'

    // Print the value stored in the pointer
    printf("Value stored in pointer ptr: %p\n", (void*)ptr);

    return 0;
}


#include <stdio.h>

int main() {
    int a = 25;       // Step 1: Original variable
    int *ptr = &a;    // Step 2: Pointer stores the address of 'a'
    int b;            // Step 3: Another variable to copy the value

    b = *ptr;         // Step 4: Copy value of 'a' into 'b' using pointer

    // Print all values to verify
    printf("Value of a: %d\n", a);
    printf("Address of a: %p\n", (void*)&a);
    printf("Value stored in pointer ptr (address of a): %p\n", (void*)ptr);
    printf("Value pointed to by ptr: %d\n", *ptr);
    printf("Value of b (copied from a using pointer): %d\n", b);

    return 0;
}


#include <iostream>
using namespace std;

int main() {
    int x = 5;        // Step 1: Declare a variable x and assign 5
    int *p = &x;      // Step 2: Pointer p stores the address of x

    *p = 5;           // Step 3: Dereference pointer p and assign 5 to x

    // Step 4: Print the value of x and value pointed to by p
    cout << "Value of x: " << x << endl;
    cout << "Value pointed to by p: " << *p << endl;

    return 0;
}
