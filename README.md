# lab7
#include <stdio.h>
#include <string.h>


int main()
{
    int n, arr[100], i, max, k, sum;     
    printf("Введите число элементов массива=");
    scanf("%d", &n);   
    printf("Введите элементы массива :");
    for(i = 0 ; i < n ; i++) {
    scanf("%d", &arr[i]);    
    }
    max = arr[0];                   
    for(i = 1 ; i < n ; ++i)     
    {
       if (arr[i] > max) 
       {
           max = arr[i];           
       }
       if (arr[i] > 0){
           k = i;
       }
    }
    sum = 0;
    for (int i = 0; i <= k; i++)
    {
        sum += arr[i];
    }
    printf("1) Max = %d", max);
    printf("\n2) Sum = %d", sum);
    //3)
    int a, b;
    printf("\nВведите a = ");
    scanf("%d", &a);
    printf("\nВведите b = ");
    scanf("%d", &a);
    int j = i;
    for (int i = 0; i < n; i++)
    {
    if (arr[i] < a || arr[i] > b){
        arr[i - j] = arr[i];
    else{
        j++;}
}
}
    for (i = n - j; i < n; i++){
        arr[i] = 0;
        printf("3) %d ", arr[j]);
}
    return 0;
}
