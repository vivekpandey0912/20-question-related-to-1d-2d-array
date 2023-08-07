Sure, I can provide you with 20 Java programs for both 1D and 2D arrays that can be useful for interview preparation. Here they are:

**1D Array Programs:**

1. **Sum of Array Elements:**
```java
public class SumArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int sum = 0;
        for (int num : arr) {
            sum += num;
        }
        System.out.println("Sum of array elements: " + sum);
    }
}
```

2. **Find Maximum Element:**
```java
public class MaxArray {
    public static void main(String[] args) {
        int[] arr = {10, 5, 20, 8, 15};
        int max = arr[0];
        for (int num : arr) {
            if (num > max) {
                max = num;
            }
        }
        System.out.println("Maximum element: " + max);
    }
}
```

3. **Search Element:**
```java
public class SearchArray {
    public static void main(String[] args) {
        int[] arr = {10, 5, 20, 8, 15};
        int searchElement = 20;
        boolean found = false;
        for (int num : arr) {
            if (num == searchElement) {
                found = true;
                break;
            }
        }
        System.out.println("Element found: " + found);
    }
}
```

4. **Array Rotation:**
```java
public class RotateArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int rotations = 2;
        int n = arr.length;
        int[] rotated = new int[n];
        for (int i = 0; i < n; i++) {
            rotated[(i + rotations) % n] = arr[i];
        }
        System.out.println("Rotated array: " + Arrays.toString(rotated));
    }
}
```

5. **Reverse Array:**
```java
public class ReverseArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int n = arr.length;
        for (int i = 0; i < n / 2; i++) {
            int temp = arr[i];
            arr[i] = arr[n - i - 1];
            arr[n - i - 1] = temp;
        }
        System.out.println("Reversed array: " + Arrays.toString(arr));
    }
}
```

6. **Check Palindrome Array:**
```java
public class PalindromeArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 2, 1};
        boolean palindrome = true;
        int n = arr.length;
        for (int i = 0; i < n / 2; i++) {
            if (arr[i] != arr[n - i - 1]) {
                palindrome = false;
                break;
            }
        }
        System.out.println("Array is palindrome: " + palindrome);
    }
}
```

7. **Remove Duplicates:**
```java
public class RemoveDuplicates {
    public static void main(String[] args) {
        int[] arr = {1, 2, 2, 3, 4, 4, 5};
        int n = arr.length;
        int newSize = 0;
        for (int i = 0; i < n - 1; i++) {
            if (arr[i] != arr[i + 1]) {
                arr[newSize++] = arr[i];
            }
        }
        arr[newSize++] = arr[n - 1];
        System.out.println("Array after removing duplicates: " + Arrays.toString(Arrays.copyOf(arr, newSize)));
    }
}
```

8. **Find Second Largest Element:**
```java
public class SecondLargest {
    public static void main(String[] args) {
        int[] arr = {10, 5, 20, 8, 15};
        int max = arr[0];
        int secondMax = Integer.MIN_VALUE;
        for (int num : arr) {
            if (num > max) {
                secondMax = max;
                max = num;
            } else if (num > secondMax && num != max) {
                secondMax = num;
            }
        }
        System.out.println("Second largest element: " + secondMax);
    }
}
```

9. **Sort Array in Ascending Order:**
```java
public class ArraySort {
    public static void main(String[] args) {
        int[] arr = {5, 2, 8, 1, 3};
        Arrays.sort(arr);
        System.out.println("Sorted array: " + Arrays.toString(arr));
    }
}
```

10. **Find Missing Number in Array:**
```java
public class MissingNumber {
    public static void main(String[] args) {
        int[] arr = {1, 2, 4, 5};
        int n = arr.length + 1;
        int totalSum = (n * (n + 1)) / 2;
        int actualSum = 0;
        for (int num : arr) {
            actualSum += num;
        }
        int missingNumber = totalSum - actualSum;
        System.out.println("Missing number: " + missingNumber);
    }
}
```

**2D Array Programs:**

1. **Matrix Addition:**
```java
public class MatrixAddition {
    public static void main(String[] args) {
        int[][] matrix1 = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
        int[][] matrix2 = {{9, 8, 7}, {6, 5, 4}, {3, 2, 1}};
        int rows = matrix1.length;
        int cols = matrix1[0].length;
        int[][] sumMatrix = new int[rows][cols];
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                sumMatrix[i][j] = matrix1[i][j] + matrix2[i][j];
            }
        }
        System.out.println("Sum of matrices:");
        for (int[] row : sumMatrix) {
            System.out.println(Arrays.toString(row));
        }
    }
}
```

2. **Matrix Multiplication:**
```java
public class MatrixMultiplication {
    public static void main(String[] args) {
        int[][] matrix1 = {{1, 2}, {3, 4}};
        int[][] matrix2 = {{5, 6}, {7, 8}};
        int rows1 = matrix1.length;
        int cols1 = matrix1[0].length;
        int cols2 = matrix2[0].length;
        int[][] productMatrix = new int[rows1][cols2];
        for (int i = 0; i < rows

1; i++) {
            for (int j = 0; j < cols2; j++) {
                for (int k = 0; k < cols1; k++) {
                    productMatrix[i][j] += matrix1[i][k] * matrix2[k][j];
                }
            }
        }
        System.out.println("Product of matrices:");
        for (int[] row : productMatrix) {
            System.out.println(Arrays.toString(row));
        }
    }
}
```

3. **Transpose of a Matrix:**
```java
public class MatrixTranspose {
    public static void main(String[] args) {
        int[][] matrix = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
        int rows = matrix.length;
        int cols = matrix[0].length;
        int[][] transposeMatrix = new int[cols][rows];
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                transposeMatrix[j][i] = matrix[i][j];
            }
        }
        System.out.println("Transpose of matrix:");
        for (int[] row : transposeMatrix) {
            System.out.println(Arrays.toString(row));
        }
    }
}
```

4. **Find Maximum Element in 2D Array:**
```java
public class Max2DArray {
    public static void main(String[] args) {
        int[][] matrix = {{10, 5, 20}, {8, 15, 25}, {12, 18, 30}};
        int max = matrix[0][0];
        for (int[] row : matrix) {
            for (int num : row) {
                if (num > max) {
                    max = num;
                }
            }
        }
        System.out.println("Maximum element: " + max);
    }
}
```

5. **Spiral Traversal of Matrix:**
```java
public class SpiralTraversal {
    public static void main(String[] args) {
        int[][] matrix = {{1, 2, 3, 4}, {5, 6, 7, 8}, {9, 10, 11, 12}};
        int rows = matrix.length;
        int cols = matrix[0].length;
        int top = 0, bottom = rows - 1, left = 0, right = cols - 1;
        while (top <= bottom && left <= right) {
            for (int i = left; i <= right; i++) {
                System.out.print(matrix[top][i] + " ");
            }
            top++;
            for (int i = top; i <= bottom; i++) {
                System.out.print(matrix[i][right] + " ");
            }
            right--;
            if (top <= bottom) {
                for (int i = right; i >= left; i--) {
                    System.out.print(matrix[bottom][i] + " ");
                }
                bottom--;
            }
            if (left <= right) {
                for (int i = bottom; i >= top; i--) {
                    System.out.print(matrix[i][left] + " ");
                }
                left++;
            }
        }
    }
}
```

6. **Rotate Matrix 90 Degrees:**
```java
public class RotateMatrix {
    public static void main(String[] args) {
        int[][] matrix = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
        int rows = matrix.length;
        int cols = matrix[0].length;
        int[][] rotatedMatrix = new int[cols][rows];
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                rotatedMatrix[j][rows - i - 1] = matrix[i][j];
            }
        }
        System.out.println("Rotated matrix:");
        for (int[] row : rotatedMatrix) {
            System.out.println(Arrays.toString(row));
        }
    }
}
```

7. **Find Diagonal Sum of Matrix:**
```java
public class DiagonalSum {
    public static void main(String[] args) {
        int[][] matrix = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
        int n = matrix.length;
        int primaryDiagonalSum = 0;
        int secondaryDiagonalSum = 0;
        for (int i = 0; i < n; i++) {
            primaryDiagonalSum += matrix[i][i];
            secondaryDiagonalSum += matrix[i][n - i - 1];
        }
        System.out.println("Primary diagonal sum: " + primaryDiagonalSum);
        System.out.println("Secondary diagonal sum: " + secondaryDiagonalSum);
    }
}
```

8. **Find Frequency of Element in Matrix:**
```java
public class ElementFrequency {
    public static void main(String[] args) {
        int[][] matrix = {{1, 2, 3}, {4, 2, 6}, {2, 8, 9}};
        int target = 2;
        int frequency = 0;
        for (int[] row : matrix) {
            for (int num : row) {
                if (num == target) {
                    frequency++;
                }
            }
        }
        System.out.println("Frequency of element " + target + ": " + frequency);
    }
}
```

9. **Check Identity Matrix:**
```java
public class IdentityMatrix {
    public static void main(String[] args) {
        int[][] matrix = {{1, 0, 0}, {0, 1, 0}, {0, 0, 1}};
        boolean isIdentity = true;
        int n = matrix.length;
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                if (i == j && matrix[i][j] != 1) {
                    isIdentity = false;
                    break;
                } else if (i != j && matrix[i][j] != 0) {
                    isIdentity = false;
                    break;
                }
            }
        }
        System.out.println("Matrix is identity: " + isIdentity);
    }
}
```

10. **Find Common Elements in Rows:**
```java
public class CommonElementsInRows {
    public static void main(String[] args) {
        int[][] matrix = {{1, 2, 3}, {4, 2, 6}, {2, 8, 9}};
        int rows = matrix.length;
        int cols = matrix[0].length;
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                boolean isCommon = true;
                for (int k = 0; k < rows; k++) {
                    if (matrix[k][j] != matrix[i][j]) {
                        isCommon = false;
                        break;
                    }
                }
                if (isCommon) {
                    System.out.println("Common element in row " + i + ": "

 + matrix[i][j]);
                }
            }
        }
    }
}
```

Feel free to use these Java programs to practice and prepare for interviews. Each program covers a specific concept and can help you gain a better understanding of working with 1D and 2D arrays. Remember to study and modify these programs to suit your learning needs.
