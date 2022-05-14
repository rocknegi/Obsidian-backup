# About 
```
void insertionSort(int arr[],int n){ 
  for(int i=1;i<n;i++){
      for(int j=i;j>0;j--){
          if(isGreater(arr,j-1,j)){
              swap(arr,j-1,j);
          }
          else break;
      }
  }
    
}
```

We'll use the following array as an example: 2, 9, 5, 1, 3. 
The insertion sort will be broken down into steps. But first, keep in mind that "an array of size one is always sorted." There is no other number to compare with if there is only one element, hence it is always sorted (both increasing and decreasing). As a result, we must conduct operations on the remaining four digits. Iterations will be n-1 for n integers.

- We'll figure out where 9 is in only 2, 9 seconds. It will be placed after 9 because 9 is greater than 2. So [2, 9] will be the final order.
-  In just 2, 9, 5, we shall determine the position of 5. Because 5 is between 2 and 9, it will be positioned as [2, 5, 9]. HOW? We'll talk about it later. 
-  The position of 1 in 2, 5, 9, 1 will have to be determined. Because 1 is the smallest, it will be placed first. As a result, the ultimate order is [1, 2, 5, 9]. 
-   Now we'll figure out where 3 belongs in the numbers 1, 2, 5, and 9, and 3 will be between 2 and 5. So [1, 2, 3, 5, 9] is the final order.



![Segun Adebayo](https://s3.ap-south-1.amazonaws.com/feed-resources-dev/f6e8f354-b1a9-4903-9dc0-5c605138d18f/articles/image/138d0450-f42b-40c7-ba7e-ab29ceb1d090.png)


# Analysis:

### Time Complexity :

- O(n^2) We're only running two loops. What do you believe the worst case scenario for Insertion sort will be? Yes, if all of the numbers are arranged backwards (in descending order). 
- Then we'll have to do 1+ 2 + 3 +... swaps for each iteration of n-1. So, this is an Arithmetic Progression with the outcome n*(n+1)/2 = n^2. 
- Worst-case scenario: O (n^2). 
- Best Case: O(n) 

### Space Complexity :

O(1) Because the only core operation is a swap, we're working with constant auxiliary space.