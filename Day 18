#include <stdio.h>
#include <stdlib.h>

int diagonalDifference(int **arr, int n) {
    int primaryDiagonalSum = 0, secondaryDiagonalSum = 0;

    for (int i = 0; i < n; i++) {
        primaryDiagonalSum += arr[i][i];           
        secondaryDiagonalSum += arr[i][n - i - 1]; 
    }

    return abs(primaryDiagonalSum - secondaryDiagonalSum);
}

int main() {
    int n;
    scanf("%d", &n);

    int **arr = (int **)malloc(n * sizeof(int *));
    for (int i = 0; i < n; i++) {
        arr[i] = (int *)malloc(n * sizeof(int));
    }
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            scanf("%d", &arr[i][j]);
        }
    }

    int result = diagonalDifference(arr, n);
    printf("%d\n", result);

    for (int i = 0; i < n; i++) {
        free(arr[i]);
    }
    free(arr);

    return 0;
}
