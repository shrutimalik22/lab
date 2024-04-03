include <stdio.h>

int linear_search(int arr[], int n, int key, int *comparisons) {
    for (int i = 0; i < n; i++) {
        (*comparisons)++;
        if (arr[i] == key) {
            return 1; // Element found
        }
    }
    return 0; // Element not found
}

int main() {
    int arr[] = {3, 5, 1, 9, 7, 2, 8, 4, 6};
    int n = sizeof(arr) / sizeof(arr[0]);
    int key = 7;
    int comparisons = 0;

    int found = linear_search(arr, n, key, &comparisons);

    if (found) {
        printf("Element found!\n");
    } else {
        printf("Element not found.\n");
    }
    printf("Total comparisons: %d\n", comparisons);

    return 0;
}
