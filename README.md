# 2DMatrix.cpp

This C++ program allows users to create a 2D matrix, specify the number of rows and columns, initialize the matrix with custom values, and display the resulting matrix.

## Code

The code provided here includes functions for:

- Creating a 2D matrix.
- Initializing the matrix with user-defined values.
- Displaying the matrix.

## Usage

To create and manipulate a 2D matrix, follow these steps:

1. Include the necessary header files.
2. Specify the number of rows and columns when prompted by the program.
3. The program will initialize the matrix with values incrementing from 1.
4. The program will display the matrix.

## Code Example

```cpp
#include <iostream>
#include <vector>

using namespace std;

// Function to create a 2D matrix
vector<vector<int>> createMatrix(int rows, int columns) {
    return vector<vector<int>>(rows, vector<int>(columns, 0));
}

// Function to initialize the matrix with values
void initializeMatrix(vector<vector<int>>& matrix) {
    // Your initialization logic here
    int value = 1;
    for (int i = 0; i < matrix.size(); i++) {
        for (int j = 0; j < matrix[0].size(); j++) {
            matrix[i][j] = value;
            value++;
        }
    }
}

// Function to display the matrix
void displayMatrix(const vector<vector<int>>& matrix) {
    for (int i = 0; i < matrix.size(); i++) {
        for (int j = 0; j < matrix[0].size(); j++) {
            cout << matrix[i][j] << " ";
        }
        cout << endl;
    }
}

int main() {
    int rows, columns;

    cout << "Enter the number of rows: ";
    cin >> rows;

    cout << "Enter the number of columns: ";
    cin >> columns;

    vector<vector<int>> matrix = createMatrix(rows, columns);
    initializeMatrix(matrix);

    cout << "2D Matrix:" << endl;
    displayMatrix(matrix);

    return 0;
}
