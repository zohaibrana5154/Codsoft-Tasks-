# Codsoft-Tasks-Create a simple calculator in C++.
#include <iostream>
using namespace std;


double add(double num1, double num2);
double subtract(double num1, double num2);
double multiply(double num1, double num2);
double divide(double num1, double num2);

int main() {
    double num1, num2;
    char operation;

    cout << "Simple Calculator\n";
    cout << "Enter the first number: ";
    cin >> num1;

    cout << "Enter the operation (+, -, *, /): ";
    cin >> operation;

    cout << "Enter the second number: ";
    cin >> num2;

    double result;
    switch (operation) {
        case '+':
            result = add(num1, num2);
            break;
        case '-':
            result = subtract(num1, num2);
            break;
        case '*':
            result = multiply(num1, num2);
            break;
        case '/':
            if (num2 == 0) {
                cout << "Error: Cannot divide by zero.\n";
                return 1;
            }
            result = divide(num1, num2);
            break;
        default:
            cout << "Invalid operation.\n";
            return 1;
    }

    cout << "Result: " << result << endl;
    return 0;
}

double add(double num1, double num2) {
    return num1 + num2;
}

double subtract(double num1, double num2) {
    return num1 - num2;
}

double multiply(double num1, double num2) {
    return num1 * num2;
}

double divide(double num1, double num2) {
    return num1 / num2;
}
