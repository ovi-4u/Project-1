#include <stdio.h>
#define SIZE 100
void showArray(int arr[], int size) {
    printf("Current array: ");
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}
void insertAt(int arr[], int *size, int position, int value) {
    if (*size >= SIZE) {
        printf("Array is full. Cannot add more elements.\n");
        return;
    }
    for (int i = *size; i > position; i--) {
        arr[i] = arr[i - 1];
    }
    arr[position] = value;
    (*size)++;
}
void updateValue(int arr[], int position, int newValue) {
    arr[position] = newValue;
}
void deleteAt(int arr[], int *size, int position) {
    for (int i = position; i < *size - 1; i++) {
        arr[i] = arr[i + 1];
    }
    (*size)--;
}
int findIndex(int arr[], int size, int value) {
    for (int i = 0; i < size; i++) {
        if (arr[i] == value) {
            return i;
        }
    }
    return -1;
}
int main() {
    int arr[SIZE] = {10, 25, 35, 45, 55};
    int size = 5;

    showArray(arr, size);

    insertAt(arr, &size, 2, 20);
    showArray(arr, size);

    updateValue(arr, 3, 30);
    showArray(arr, size);

    deleteAt(arr, &size, 4);
    showArray(arr, size);

    int index = findIndex(arr, size, 30);
    if (index != -1) {
        printf("Value 30 found at index %d\n", index);
    } else {
        printf("Value 30 not found in the array.\n");
    }
    return 0;
}
