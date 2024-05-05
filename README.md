# Simple-loops
#include <iostream>
using namespace std;

// Function to print the Fibonacci sequence up to n terms using loops
void printFibonacciIterative(int n) {
    int a = 0, b = 1, c;
    if (n >= 1) cout << a << " ";  // Print the first Fibonacci number
    if (n >= 2) cout << b << " ";  // Print the second Fibonacci number
    
    for(int i = 3; i <= n; ++i) {
        c = a + b;  // Next Fibonacci number is the sum of the previous two
        cout << c << " ";
        a = b;  // Update the first of the pair
        b = c;  // Update the second of the pair
    }
    cout << endl;
}

int main() {
    int n;
    cout << "Enter the number of terms of Fibonacci sequence to display: ";
    cin >> n;
    printFibonacciIterative(n);
    return 0;
}
