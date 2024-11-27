# linear-search
#include <stdio.h>


int linearSearch(int array[], int n, int key) {
    for (int i = 0; i < n; i++) { 
        if (array[i] == key) {   
            return i;           
        }
    }
    return -1;                   
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
