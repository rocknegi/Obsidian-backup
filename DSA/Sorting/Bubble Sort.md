## About
- It compares the current element with the next one and swap if the next element is smaller than the current one
- After every iteration we don't iterate to the last element that was already checked in the previous iteration.

```
	void bubbleSort(int arr[],int n){
    for(int i = 0; i<n; i++){
        for(int j=0; j<n-1-i; j++){
            if(isSmaller(arr,j+1,j))
                swap(arr,j+1,j);
        }
    }
    }
```

![Segun Adebayo](https://s3.ap-south-1.amazonaws.com/feed-resources-dev/1d7cc7cc-b8ab-4cfd-abc5-369bfdf12f3c/articles/image/0168acd8-20a0-46b8-8b6a-f89f8503f158.png)

![Segun Adebayo](https://s3.ap-south-1.amazonaws.com/feed-resources-dev/1d7cc7cc-b8ab-4cfd-abc5-369bfdf12f3c/articles/image/263280a1-a6d8-454d-aa27-17d93faba056.png)

##  ANALYSIS
Time complexity O( N^2 ). 
Space complexity O(1)