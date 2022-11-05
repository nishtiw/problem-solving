# Rotate Array 
- [Problem Link](https://practice.geeksforgeeks.org/problems/rotate-array-by-n-elements-1587115621/1?utm_source=gfg&utm_medium=article&utm_campaign=bottom_sticky_on_article)
- [Solution](https://www.youtube.com/watch?v=PgC0cOA_Ylg&ab_channel=CodeIn10-NishantChahar)

## My Solution 
```
class Solution
{
    //Function to rotate an array by d elements in counter-clockwise direction. 

    static void rotateArr(int arr[], int d, int n)

    {

        // add your code here
        d = d%n;
        int a2[] = arr.clone();
        int d2 = d;
        int i=0;
        while(d2!=n) {
            arr[i] = a2[d2];
            i++;
            d2++;
        }
        int j=0;
        while(j!=d) {
            arr[i] = a2[j];
            i++;
            j++;
        }
    }

}
```

## Optimal Solution
```
class Solution
{
    //Function to rotate an array by d elements in counter-clockwise direction. 
    public static void reverse(int arr[],int a,int b){

        while(a<b){

            int temp=arr[a];

            arr[a]=arr[b];

            arr[b]=temp;

            a++;b--;

        }

    }

    static void rotateArr(int arr[], int d, int n)

    {

        // add your code here 

        d=d%n;

        reverse(arr,0,d-1);

        reverse(arr,d,n-1);

        reverse(arr,0,n-1);
    }

}
```
