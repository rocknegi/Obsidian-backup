# About

Clearly, we have i pointing to 2 and j pointing to 7. Now 2<7, so final[k] = 2, and since we considered 2 we will increment i and also k. k will always be incremented.

![img](https://pepvids.sgp1.cdn.digitaloceanspaces.com/articles/merge_two_sorted_arrays%20/merge_two_sorted_arrays_1.png)

Now we compare 5 and 7. Again 5 is smaller so final[k] = final[1] = 5. And i and k will be incremented.

![img](https://pepvids.sgp1.cdn.digitaloceanspaces.com/articles/merge_two_sorted_arrays%20/merge_two_sorted_arrays_2.png)

This time between 12 and 7. 7 is smaller. So final[k] = final[2] = 7. And since an element of arr2 was chosen we will increment j. k will always be incremented as we mentioned before.

![img](https://pepvids.sgp1.cdn.digitaloceanspaces.com/articles/merge_two_sorted_arrays%20/merge_two_sorted_arrays_3.png)

This time between 12 and 9. 9 is smaller. So final[k] = final[3] = 9. And since an element of arr2 was chosen we will increment j. k will always be incremented as always.

![img](https://pepvids.sgp1.cdn.digitaloceanspaces.com/articles/merge_two_sorted_arrays%20/merge_two_sorted_arrays_4.png)

You can clearly see we are slowly moving across the arrays and building a new merged array which is also in sorted order by making greedy decisions at every point of choosing the smaller value.

# Code
```
vector<int> mergeTwoSortedArrays(vector<int> &A, vector<int> &B)
{
    int i = 0;
    int j = 0;
    int k = 0;
    vector<int> res(A.size() + B.size());

    while (i < A.size() && j < B.size())
    {
        if (A[i] < B[j])
        {
            res[k] = A[i];
            i++;
        }
        else
        {
            res[k] = B[j];
            j++;
        }
        k++;
    }  
        for (; i < A.size(); i++)
        {
            res[k] = A[i];
            k++;
        }    
        for (; j < B.size(); j++)
        {
            res[k] = B[j];
            k++;
        }
    return res;
}

```

# Analysis

Time Complexity :

**O(n)**

- Time complexity will be O(n) where n = a.length + b.length because if we look at i it will move from 0 to a.length only once. And j will move from 0 to b.length only once. 
- So total iterations is a.length + b.length. If you are still not impressed, look at k. k will loop throughout the result array only once. Hence from here also we can say that the time complexity will be a.length + b.length i.e linear O(n).

SPACE COMPLEXITY :

**O(n)**

- Here we are actually using a temporary array of size a.length + b.length to store the merged array. So our space complexity is **O(n)** i.e Linear.