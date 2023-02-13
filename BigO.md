# big O

 - **O(1)** - constant (does not contain loops)
 - **O(log n)** - searching operations
 - **O(n)** - Linear, loops (for, while)
 - **O(n*log(n))** - Sorting operations
 - **O(n^2)** - two nested loops
 - **O(2^n)** - recursive algorithm
 - **O(n!)** - Adding loop for every element

## Rules:

 1. Always check for worst case
 2. Remove constants
 3. different inputs should have different variables
 4. Drop non dominant terms

## Time complexity reasons:
- Operations (+, - , *, /)
- Comparisons (<, >, ==)
- Loops (fro, while)
-  Outside function calls 

## Space complexity reasons:
- Variables
-  Data Structures
-  Function calls
-  Allocations

<br>

[![](https://paper-attachments.dropbox.com/s_2D428973624E7FC84C7D69D11421DE762BEA6B6F3361231FCDCAE0425D14526F_1664885448372_Untitled.drawio+17.png)](http://https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.freecodecamp.org%2Fnews%2Fbig-o-cheat-sheet-time-complexity-chart%2F&psig=AOvVaw3hvG4CXwZ7X0619C39dQQO&ust=1671272588429000&source=images&cd=vfe&ved=0CBAQjRxqFwoTCNjHkdn1_fsCFQAAAAAdAAAAABAN)

<br>

### Time complexity

```java
class bigo 
{
  public static void main(String args[]) 
  {
    mymethod();
  }
  static void mymethod() 
  {
    int a = 10; 				//O(1)
    a = 50 + 3; 				 //O(1)
    for (int i = 0; i < 10; i++)				//O(n)
    {
      a++;				//O(n)
      System.out.println(a);				//O(n)
    }
  }
}

```
The notation is: `O(2+ 3n)`
according to rule we drop the constants and remove the non dominant terms,
hence the notation is: `O(n)`
<br>


```java

class bigo 
{
  public static void main(String args[]) 
  {
    int arr[] =  {1,3,4,5,6};
    int arr1[] = {3,4,3,2,2};
    mymethod(arr, arr1);
  }
  static void mymethod(int a[], int b[]) 
  {
    for(int i=0;i<a.length;i++) 				//O(n)
    {
        System.out.println(a[i]);
    }
    for(int j=0;j<b.length;j++) 				//O(n)
    {
        System.out.println(b[j]);
    }
  }
}

```
The notation is: `O(a + b)` because according to the rule, different inputs should have different variables (a and b are variables and any variables can be used to denote them)

<br>

> If two loops are one after the other + is used, if two loops are nested together * is used to denote them

<br>

When you see a problem where the number of elements in the
problem space gets halved each time, that will likely be a 0( log N) runtime.
This is the same reason why finding an element in a balanced binary search tree is O ( log N). With each
comparison, we go either left or right. Half the nodes are on each side, so we cut the problem space in half
each time. 

<br>

> The base of log does not matter for the purpose of Big O.

> The base of an exponent matters if you Compare 2<sup>n</sup> and 8<sup>n</sup>. If you expand 8<sup>n</sup>, you get (2<sup>3</sup>)<sup>n</sup>, which equals 2<sup>2n</sup> * 2<sup>n</sup> 
 As you can see,  and 2<sup>n</sup> and 8<sup>n</sup> are different
 
 <br>

   ```java

boolean isPrime(int n) 
{ 
 for (int x = 2; x <= sqrt(n); x++) {
	 if (n % X == 0) { 
		 return false;
	} 
} 
 return true;
 }

```
This runs on O(sqrt(n)) times
