# AlgorithmTips
Disclaimer: The following notes are taken from the book "Competitive Programmer's Handbook"
<h1>Numbers</h1>
<b>Ranges of Int:</b></br>  
- int (32 bit): -2x10^9~2x10^9</br>  
- Long long int(64 bit): -9x10^18~9x10^18</br>  
- double: 64 bit  
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
