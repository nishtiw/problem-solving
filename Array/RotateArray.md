# Rotate Array 
- [Problem Link](https://practice.geeksforgeeks.org/problems/rotate-array-by-n-elements-1587115621/1?utm_source=gfg&utm_medium=article&utm_campaign=bottom_sticky_on_article)

## My Solution 
- Throws RunTime error
```
class Solution
{
    //Function to rotate an array by d elements in counter-clockwise direction. 
    static void rotateArr(int arr[], int d, int n)
    {
        // add your code here
        int a2[] = arr.clone();
        int d2 = d;

        int i=0;
        while(d2 != n) {
            arr[i] = a2[d2];
            i++;
            d2++;
        }

        int j=0;
        while(j != d) {
            arr[i] = a2[j];
            i++;
            j++;
        }
    }
}
```

## Optimal Solution
```

```
