# Experiment8
# AIM 
To study and implement C++ 2D array matrices
# THEORY
Matrices in C++ are represented as 2D arrays. They are used to store and manipulate data in a structured, tabular form. <BR>
1) Introduction to Matrices  <BR>
A matrix is a collection of elements arranged in rows and columns.  <BR>
In C++, matrices are typically implemented using 2D arrays. <BR>

2) Declaring a Matrix <BR>
syntax for declaring a 2D array (matrix) <BR>
```
data_type matrix_name[rows][columns];
```
3) Initializing a Matrix <BR>
for eg <br>
```
int matrix[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```
4) Accessing Elements of a Matrix <br>
Elements of a matrix are accessed using row and column indices. <br>
For eg.
```
int value = matrix[1][2];
```
5) Addition of matrices :  <br>
To add two matrices in C++, you can use a nested loop structure to iterate through each element of the matrices and add corresponding elements. <br>
i) Matrix Size Input: The program asks for the number of rows and columns to define the size of the matrices. <br>
ii) Matrix Elements Input: It then prompts the user to enter the elements for the two matrices. <br>
iii) Matrix Addition: The program adds the corresponding elements of the two matrices. <br>
iv) Output: Finally, it prints the result .<br> 
6) Subtraction of matrices <br>
i) The program first asks the user to input the number of rows and columns for the matrices. <br>
ii) It then prompts the user to input the elements for both matrices. <br>
iii) The subtraction is performed by iterating through each element of the matrices and subtracting the corresponding elements. <br>
iv) The resultant matrix is then printed on the screen. <br>

# CODE AND OUTPUT 
1) A : Entering elements of matrix <br>
```
//To study and implement C++ 2D Array Matrices 
#include <iostream>
using namespace std;

int main() {
    int temp[3][3], i, j,k,l;
    for (i=0 ; i<3 ; i++){
        for (j=0;j<3;j++){
            cout<<" Enter element-("<<i<<j<<"):";
            cin>>temp[i][j];
        }
    }
    for(k-0; k<3; k++){
        for (l=0;l<3;l++){
            cout<<temp[k][l];
            cout<<" ";
    }
    cout <<endl;
    }
}
```
OUTPUT A: <BR>
![EXP8A](https://github.com/sarakanyal03/CDS_Experiment8/blob/main/EXP8A.png)
2) B : Addition of two matrices <br>
```
//Addition of two matrices
#include <iostream>
using namespace std;

int main() {
    // Define matrix dimensions
    int r1 = 3, c1 = 3;
    int r2 = 3, c2 = 3;

    int m1[r1][c1], m2[r2][c2], sum[r1][c1];

    cout << "Enter elements of the first matrix:" << endl;
    for (int i = 0; i < r1; ++i) {
        for (int j = 0; j < c1; ++j) {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m1[i][j];
        }
    }
    cout << "Enter elements of the second matrix:" << endl;
    for (int i = 0; i < r2; ++i) {
        for (int j = 0; j < c2; ++j) {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m2[i][j];
        }
    }
    for (int i = 0; i < r1; ++i) {
        for (int j = 0; j < c1; ++j) {
            sum[i][j] = m1[i][j] + m2[i][j];
        }
    }
 

    cout << endl << "Sum of matrices:" << endl;
    for (int i = 0; i < r1; ++i) {
        for (int j = 0; j < c1; ++j) {
            cout << sum[i][j] << " ";
        }
        cout << endl;
    }
    return 0;
    
}
```
OUTPUT B: <BR>
![EXP8B](https://github.com/sarakanyal03/CDS_Experiment8/blob/main/EXP8B.png)
3) C: Subtraction of two matrices <br>
```
//Subtraction of two matrices
#include <iostream>
using namespace std;

int main() {
    // Define matrix dimensions
    int r1 = 3, c1 = 3;
    int r2 = 3, c2 = 3;

    int m1[r1][c1], m2[r2][c2], difference[r1][c1];

    cout << "Enter elements of the first matrix:" << endl;
    for (int i = 0; i < r1; ++i) {
        for (int j = 0; j < c1; ++j) {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m1[i][j];
        }
    }
    cout << "Enter elements of the second matrix:" << endl;
    for (int i = 0; i < r2; ++i) {
        for (int j = 0; j < c2; ++j) {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m2[i][j];
        }
    }
    for (int i = 0; i < r1; ++i) {
        for (int j = 0; j < c1; ++j) {
            difference[i][j] = m1[i][j] - m2[i][j];
        }
    }
 

    cout << endl << "Difference of matrices:" << endl;
    for (int i = 0; i < r1; ++i) {
        for (int j = 0; j < c1; ++j) {
            cout << difference[i][j] << " ";
        }
        cout << endl;
    }
    return 0;
    
}
```
OUTPUT C: <BR>
![EXP8C](https://github.com/sarakanyal03/CDS_Experiment8/blob/main/EXP8C.png)
4) D : Multiplication of two matrices <br>
```
// Matrix multiplication 
#include <iostream>
using namespace std;

int main() {
    int r1, c1, r2, c2;
    
    // Input dimensions of the first matrix
    cout << "Enter rows and columns for the first matrix: ";
    cin >> r1 >> c1;

    // Input dimensions of the second matrix
    cout << "Enter rows and columns for the second matrix: ";
    cin >> r2 >> c2;

    // Check if matrix multiplication is possible
    if (c1 != r2) {
        cout << "Matrix multiplication not possible!" << endl;
        return 0;
    }

    // Define the matrices
    int m1[r1][c1], m2[r2][c2], result[r1][c2];

    // Input elements of the first and second matrix
    cout << "Enter elements of the first matrix:" << endl;
    for (int i = 0; i < r1; ++i) {
        for (int j = 0; j < c1; ++j) {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m1[i][j];
        }
    }
    cout << "Enter elements of the second matrix:" << endl;
    for (int i = 0; i < r2; ++i) {
        for (int j = 0; j < c2; ++j) {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m2[i][j];
        }
    } 
    // Initialize the result matrix with zeros
    for (int i = 0; i < r1; i++) {
        for (int j = 0; j < c2; j++) {
            result[i][j] = 0;
        }
    }

    // Matrix multiplication
    for (int i = 0; i < r1; i++) {
        for (int j = 0; j < c2; j++) {
            for (int k = 0; k < c1; k++) {
                result[i][j] += m1[i][k] * m2[k][j];
            }
        }
    }

    // Display the result
    cout << "Resultant matrix:\n";
    for (int i = 0; i < r1; i++) {
        for (int j = 0; j < c2; j++) {
            cout << result[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```
OUTPUT D: <BR>
![EXP8D](https://github.com/sarakanyal03/CDS_Experiment8/blob/main/EXP8D.png)
5) E : Transpose of a matrix <br>
```
#include <iostream>
using namespace std;

int main() {
    int r, c ;

    // Getting the size of the matrix
    cout << "Enter the number of rows and columns of the matrix: ";
    cin >> r  >> c ;

    int m[r][c], transpose[c][r];

    // Getting elements of the matrix
    cout << "Enter elements of the first matrix:" << endl;
    for (int i = 0; i < r; ++i) {
        for (int j = 0; j < c; ++j) {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m[i][j];
        }
    }

    // Transposing the matrix
    for(int i = 0; i < r; ++i) {
        for(int j = 0; j < c; ++j) {
            transpose[j][i] = m[i][j];
        }
    }

    // Displaying the transpose of the matrix
    cout << "\nTranspose of the matrix:" << endl;
    for(int i = 0; i < c; ++i) {
        for(int j = 0; j < r; ++j) {
            cout << transpose[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```
OUTPUT E: <BR>
![EXP8E](https://github.com/sarakanyal03/CDS_Experiment8/blob/main/EXP8E.png)
6) F : Diagnol addition of a matrix<br>

```
//DIAGONAL ADDITION 
#include <iostream>
using namespace std;


const int MAX = 100;

void printDiagonalSums(int mat[][MAX], int n) 
{ 
    int principal = 0;
    
    for (int i = 0; i < n; i++)  
    { 
        // Condition for principal diagonal 
        principal += mat[i][i]; 
    } 
  
    cout << "Sum of the diagonal elements is: " << principal << endl; 
} 

int main() 
{ 
    int a[][MAX] = {{1, 2, 3, 4},  
                    {5, 6, 7, 8},  
                    {1, 2, 3, 4},  
                    {5, 6, 7, 8}}; 
    printDiagonalSums(a, 4); 
return 0;
}
```
OUTPUT F: <BR>
![EXP8F](https://github.com/sarakanyal03/CDS_Experiment8/blob/main/EXP8F.png)

# CONCLUSION
This experiment provides valuable insight into fundamental concepts in programming, particularly in handling data structures that require multi-dimensional organization. Through this process, we gain a deeper understanding of how to: <br>

* Efficiently Store and Manipulate Data: Using 2D arrays, we can efficiently store data in a tabular format, making it easier to perform operations like addition, subtraction, and multiplication of matrices.

* Develop Problem-Solving Skills: Implementing matrix operations enhances logical thinking and problem-solving skills, as it requires careful consideration of indices, loops, and data handling.

* Understand Memory Management: Working with 2D arrays in C++ also provides an understanding of how memory is allocated and accessed in programming, especially in managing rows and columns of data.

* Apply Concepts in Real-World Scenarios: Matrix operations are fundamental in various fields such as engineering, computer graphics, machine learning, and scientific computing. Understanding how to implement these in C++ prepares us to tackle more complex problems in these domains.
