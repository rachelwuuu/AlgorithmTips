# AlgorithmTips
Disclaimer: The following notes are taken from the book "Competitive Programmer's Handbook" by Antti Laaksonen. Available at: https://cses.fi/book/book.pdf
<h1>Numbers</h1>
<b>Ranges of Int:</b></br>  
- int (32 bit): -2x10^9~2x10^9</br>  
- Long long int(64 bit): -9x10^18~9x10^18</br>  
- double: 64 bit</br>  
- long double: 80 bit   
 
<b>Given:</b>  
❌int a=123456789;  
long long b = a * a;  
✔long a = 123456789;  
long long b = a * a;  
✔int a=123456789;  
long long b = (long long) a * a;  

<b>Comparing Two Floating Numbers:</b>  
❌if(a==b)  
✔if(abs(a-b)<1e-9)
- Difficulty: Some numbers can not be represented accurately.</BR>
  eg. double x = 0.3 * 3 + 0.1;
      printf("%.20f\n", x); //0.99999999999999988898

<b>Shortening code</b>  
eg. typedef vector <int<int>> vi;  
typedef pair <int, int> pi;  

<b>Sum formulas</b>  </br>
- sum of x from 1 to n = n(n+1)/2  
- sum of x^2 from 1 to n = n(n+1)(2n+1)/6  
- sum of n numbers where the difference between two consecutive numbers is constant a+...+b (in order) = n(a+b)/2
- sum of n numbers where the ratio k between two consecutive numbers is constant a+ak+...+b (in order) = (bk-a)/(k-1)
- Fibonacci Numbers: f(0)=0, f(1)=1, f(n)=f(n-1)+f(n-2)  
  Binet's formula: f(n)=((1 + sqrt(5))^n - (1 - sqrt(5))^n)/(2^n * sqrt(5))

<b>Logarithms</b>
- logk(ab)=logk(a)+logk(b)
- logu(x)=logk(x)/logk(u)
- The number of digits of an integer x in base b: ⌊logb(x)+1⌋  
  eg. 123 in base 2 is 1111011 and ⌊log2(123)+1⌋=7

 Complexity classes:
 - O(logn): log2n equals the number of times n must be divided by 2 to get 1.
 - O(2^n): Indicates that the algorithm iterates through all subsets of the input elements. eg. subsets of {1,2,3} are ∅, {1}, {2}, {3}, {2,3}, {1,3}, {1,2}, {1,2,3}
 - O(n!): Indicates iteration through all permutations of the input elements. eg. permutations of {1,2,3} are (1,2,3), (1,3,2), (2,1,3), (2,3,1), (3,2,1), (3,1,2)
 
 <table>
     <tr>
      <th>input size</th>
      <th>required time complexity</th>
     </tr>
     <tr>
      <th>n<=10</th>
       <th>O(n!)</th>
     </tr>
     <tr>
      <th>n<=20</th>
       <th>O(2^n)</th>
     </tr>
      <tr>
      <th>n<=500</th>
       <th>O(n^3)</th>
     </tr>
     <tr>
      <th>n<=5000</th>
       <th>O(n^2)</th>
     </tr>
     <tr>
      <th>n<=10^6</th>
       <th>O(nlogn) or O(n)</th>
     </tr>
     <tr>
      <th>n is large</th>
       <th>O(1) or O(logn)</th>
     </tr>
 </table>

 <h1>Sorting Algorithms</h1>
 	• O(n^2): Bubble Sort, an algorithm that always swaps consecutive elements in the array.  </br>
 	• O(nlogn): Merge Sort. If a=b, don't do anything, because subarray is already sorted. Calculate the position of the middle element: k=⌊(a+b)/2⌋. Recursively sort the subarray array[a...k]. Recursively sort the subarray array[k+1...b]. Merge the sorted array array[a...k] and array[k+1...b] into a sorted subarray array[a...b] </br>
 	• O(n): Counting Sort, an algorithm that calculates how many times an element appears in the array.</br>
 	• C++ sort function:  </br>
     	- sort(myVectorOrString.begin(), myVectorOrString.end()): sort a vector/string in increasing order.   </br>
     	- sort(myVectorOrString.rbegin(), myVectorOrString.rend()): sort a vector/string in decreasing order. </br>
      - vector<>pair<int,int> v;</br>
        v.push_back(1,6);</br>...</br>
        sort(v.begin(), v.end()); //sort by the first int, then by second int, etc. same for tuple<int, int, int<int>></br>
       
