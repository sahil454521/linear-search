# linear-search
#include <stdio.h>

// Function to perform linear search
int linearSearch(int array[], int n, int key) {
    for (int i = 0; i < n; i++) { // Loop from 0 to n-1
        if (array[i] == key) {    // Check if current element matches the key
            return i;             // Return the index if key is found
        }
    }
    return -1;                    // Return -1 if the key is not found
}

int main() {
    int n, key;

   
   printf("Enter the size of the array: ");
    scanf("%d", &n);
    int array[n];
 printf("Enter %d elements of the array:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &array[i]);
    }
printf("Enter the key to search: ");
scanf("%d", &key);

   int result = linearSearch(array, n, key);
if (result != -1) {
        printf("Key found at index %d.\n", result);
    } else {
        printf("Key not found in the array.\n");
    }

  return 0;
}
