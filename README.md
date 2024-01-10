Maximum scalar products of two vectors in C++
Here, in this page we will discuss the program to find maximum scalar products of two vectors in C++ programming language. Scalar product is also known as dot product.In this page we will discuss the two different ways to find the maximum dot product.

 

maximum scalar product
While loop in C
Method Discussed :
Method 1 : Without using inbuilt sort() function for sorting.
Method 2 : Using sort() function for sorting.
Let’s discuss both methods one by one in brief,

Method 1 :
Sort the first array in ascending order,
Sort the second array in ascending order.
Declare a variable say product = 0.
Run a loop from index 0 to n
Set product += (arrr1[i]*arr2[i])
After complete iteration print product.
Time and Space Complexity :
Time Complexity : O(n2)
Space Complexity : O(1)
Method 1 : Code in C++
Run
#include<bits/stdc++.h>
using namespace std;

int main(){

   int arr1[] = {1, 2, 6, 3, 7};
   int arr2[] = {10, 7, 45, 3, 7};

   int n = sizeof(arr1)/sizeof(arr1[0]);


   //Sort arr1 in ascending order
   for(int i=0; i<n; i++){
       for(int j=i+1; j<n; j++){ if(arr1[i]>arr1[j]){
               int temp = arr1[i];
               arr1[i] = arr1[j];
               arr1[j] = temp;
           }
       }
   }

   //Sort arr2 in ascending order
   for(int i=0; i<n; i++){
       for(int j=i+1; j<n; j++){ if(arr2[i]>arr2[j]){
                int temp = arr2[i];
                arr2[i] = arr2[j];
                arr2[j] = temp;
           }
       }
    }

    int product = 0;
    for(int i=0; i<n; i++)
        product += arr1[i]*arr2[i];

    cout<< product;

}
Output
413
Related Pages
Removing Duplicate elements from an array

Finding Minimum scalar product of two vectors

Counting the number of even and odd elements in an array 

Find all Symmetric pairs in an array 

Find maximum product sub-array in a given array

Method 2 :
In this method we will use inbuilt sort function to sort the array.

For, sorting arr1 in ascending order, use sort(arr1, arr1+n)
For, sorting arr2 in ascending order, use sort(arr2, arr2+n).
Time and Space Complexity :
Time Complexity : O(n log(n))
Space Complexity : O(1)
Maximum Scalar Product in C++
Method 2 : Code in C++
Run
#include<bits/stdc++.h>
using namespace std;

int main(){

   int arr1[] = {1, 2, 6, 3, 7};
   int arr2[] = {10, 7, 45, 3, 7};

   int n = sizeof(arr1)/sizeof(arr1[0]);


   //Sort arr1 in ascending order
   sort(arr1, arr1+n);
//Sort arr2 in ascending order
sort(arr2, arr2+n); 
int product = 0; 
for(int i=0; i<n; i++) product += arr1[i]*arr2[i]; 
cout<< product;
 }
Output
413
