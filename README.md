#include <stdio.h>
#include <stdlib.h>
int main() {
    int n;
    printf("Nhap so phan tu n: ");
    scanf("%d", &n);
    if (n <= 0) {
        printf("So phan tu phai lon hon 0!\n");
        return 1;
    }
    float *arr = malloc(n * sizeof(float));
    if (arr == NULL) {
        printf("Khong du bo nho!\n");
        return 1;
    }
    // 3. Nhập mảng
    for (int i = 0; i < n; i++) {
        printf("Nhap phan tu arr[%d]: ", i);
        scanf("%f", arr + i);
    }
    printf("\nMang vua nhap: ");
    for (int i = 0; i < n; i++) {
        printf("%.2f ", *(arr + i));
    }
    printf("\n");
    free(arr);
    arr = NULL; 
    return 0;
}
