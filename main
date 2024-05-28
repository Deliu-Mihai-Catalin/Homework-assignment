#include <stdio.h>
#include <stdlib.h>

int isFeasible(int books[], int n, int k, int max_load) {
    int num_employees = 1, current_load = 0;

    for (int i = 0; i < n; i++) {
        if (books[i] > max_load) return 0;

        if (current_load + books[i] > max_load) {
            num_employees++;
            current_load = books[i];

            if (num_employees > k) return 0;
        } else {
            current_load += books[i];
        }
    }
    return 1;
}

int findMinMaxLoad(int books[], int n, int k) {
    int sum = 0;
    for (int i = 0; i < n; i++) sum += books[i];

    int left = 0, right = sum, result = sum;

    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (isFeasible(books, n, k, mid)) {
            result = mid;
            right = mid - 1;
        } else {
            left = mid + 1;
        }
    }
    return result;
}

int main() {
    int books[] = {100, 200, 300, 400, 500, 600, 700, 800, 900};
    int n = sizeof(books) / sizeof(books[0]);
    int k = 3;

    int minMaxLoad = findMinMaxLoad(books, n, k);
    printf("The minimum possible maximum load is %d\n", minMaxLoad);

    return 0;
}
