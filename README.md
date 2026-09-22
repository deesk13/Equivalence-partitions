# Equivalence Partitioning – Matrix Diagonalization

## 1. Objective

To design manual test cases using **Equivalence Partitioning** for an application that accepts a square matrix, calculates eigenvalues and eigenvectors, and determines whether the matrix is diagonalizable.

## 2. Application Requirement

### Input

A square matrix.

### Process

* Calculate eigenvalues.
* Calculate eigenvectors.
* Determine whether the matrix is diagonalizable.

### Output

If the matrix is diagonalizable, display matrices **P** and **D** such that:

$$
A = PDP^{-1}
$$

## 3. Test Input

The following 4 × 4 matrix is used:

```text
2  1  0  0
0  5  2  0
0  0  7  3
0  0  0  9
```

Since the matrix is upper triangular, its eigenvalues are the diagonal elements:

```text
λ₁ = 2
λ₂ = 5
λ₃ = 7
λ₄ = 9
```

The eigenvalues are distinct. Therefore, the matrix is diagonalizable.

## 4. Equivalence Partitions

### Valid Partitions

* Square matrix
* Numeric matrix elements
* Integer values
* Decimal values
* Diagonalizable matrix
* Valid eigenvalue/eigenvector calculation

### Invalid Partitions

* Non-square matrix
* Alphabetic values
* Special characters
* Empty matrix/input
* Invalid matrix format

## 5. Test Cases

| TC ID  | Requirement / Topic             | Test Scenario                     | Expected Result                                   | Actual Result                       |
| ------ | ------------------------------- | --------------------------------- | ------------------------------------------------- | ----------------------------------- |
| TC_001 | Matrix must be square           | Enter a valid 4×4 matrix          | Valid                                             | Matrix accepted                     |
| TC_002 | Matrix must be square           | Enter a 3×3 matrix                | Valid                                             | Matrix accepted                     |
| TC_003 | Matrix must be square           | Enter a 3×4 matrix                | Invalid                                           | Error message displayed             |
| TC_004 | Matrix must be square           | Enter a 4×3 matrix                | Invalid                                           | Error message displayed             |
| TC_005 | Matrix elements must be numeric | Enter integer values              | Valid                                             | Matrix accepted                     |
| TC_006 | Matrix elements must be numeric | Enter decimal values              | Valid                                             | Matrix accepted                     |
| TC_007 | Matrix elements must be numeric | Enter alphabetic values           | Invalid                                           | Error message displayed             |
| TC_008 | Matrix elements must be numeric | Enter special characters          | Invalid                                           | Error message displayed             |
| TC_009 | Eigenvalue calculation          | Enter the given 4×4 matrix        | Eigenvalues should be calculated                  | Eigenvalues displayed               |
| TC_010 | Eigenvector calculation         | Enter the given 4×4 matrix        | Eigenvectors should be calculated                 | Eigenvectors displayed              |
| TC_011 | Diagonalizability               | Enter a diagonalizable matrix     | Matrix should be identified as diagonalizable     | Diagonalizable result displayed     |
| TC_012 | Diagonalizability               | Enter a non-diagonalizable matrix | Matrix should be identified as non-diagonalizable | Non-diagonalizable result displayed |
| TC_013 | P and D output                  | Enter a diagonalizable matrix     | P and D should be displayed                       | P and D displayed                   |
| TC_014 | Verification                    | Enter a diagonalizable matrix     | A = PDP⁻¹ should be satisfied                     | Equation verified                   |

## 6. Testing Technique

**Equivalence Partitioning** is used to divide input data into groups or partitions where the system is expected to behave similarly.

The main partitions identified are:

* Valid square matrices
* Invalid non-square matrices
* Valid numeric values
* Invalid non-numeric values
* Diagonalizable matrices
* Non-diagonalizable matrices

## 7. Expected Outcome

The application should correctly validate the matrix input, calculate eigenvalues and eigenvectors, determine diagonalizability, and display **P** and **D** for a diagonalizable matrix.

## 8. Conclusion

Equivalence Partitioning helps reduce the number of test cases while providing coverage of important valid and invalid input classes.
