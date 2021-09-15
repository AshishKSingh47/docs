#include <stdio.h>
void bubbleSort(int arr[], int n)
{
    int i, j, temp, flag=0;
    for(i = 0; i < n; i++)
    {
        for(j = 0; j < n-i-1; j++)
        {
            if( arr[j] > arr[j+1])
            {
                temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;//Swapping happened change flag to 1
                flag = 1; //Flag to monitor swapping
            } 
        }
        if(flag==0)
        {
            break;
        }
    }
    printf("Sorted Array: ");
    for(i = 0; i < n; i++)
    {
        printf("%d  ", arr[i]); //final Sorted Array
    }
}

int main()
{
    int arr[100], i, n, step, temp;
    printf("Enter total no of elements to be sorted: "); // Size of array
    scanf("%d", &n);
 
    for(i = 0; i < n; i++)
    {
        printf("Enter element number %d: ", i+1); //elements of array
        scanf("%d", &arr[i]);
    }

    bubbleSort(arr, n); //Calling the sorting function
    
    return 0;
}
