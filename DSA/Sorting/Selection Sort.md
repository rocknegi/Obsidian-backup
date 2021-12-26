# About
- n the first iteration, our i remains fixed at 0 index that is element 5, min is also fixed at 0 index. 
- But j is initialized with i+1 i.e 1, then we compare 9 with 5, but 9 is not smaller than 5 therefore m will not update. 
- Then j is incremented to 2 and 8 is compared with 5 but 8 is not smaller than 5 therefore m will not update. 
- Then j is incremented to 3 and now 1 is compared with 5, since 1 is smaller than 5 therefore m gets updated to index 3.
- Then j is again incremented to 4 and 2 is compared with 1, since 2 is greater than 1 therefore m will remain the same. 
- After getting out of the for loop of j, m will be pointing towards the index of minimum value, i.e. 3 in this case. And then we swap value at index i and value at index m.

```
void selectionSort(int arr[],int n){
 
    for(int i=0;i<n-1;i++){
            int temp = i;
        for(int j=i;j<n-1;j++){
            if(isSmaller(arr,j+1,temp)){
                temp = j+1;
            }
        }
        swap(arr,i,temp);
    }    
}
```
![Segun Adebayo](https://s3.ap-south-1.amazonaws.com/feed-resources-dev/1336df58-fe8f-479a-9c33-22a0b2e0d850/articles/image/119b6f60-5647-4031-8553-da7e8fc39579.png)

# Analysis

- Time Complexity : Worst Case Time Complexity: O(n*n). 
- Worst case is when the array is in reverse order. 
- Best Case Time Complexity: O(n). Best case is when the input array is already sorted. 
- Average Case Time Complexity: O(n*n) The inner loop does O(n) work on each iteration, and the outer loop runs for O(n) iterations, so the total work is O(n 2). 
- SPACE COMPLEXITY : Auxiliary Space: O(1), as no extra space is used.