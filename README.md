# AlgorithmTips
Disclaimer: The following notes are taken from the book "Competitive Programmer's Handbook"
<h1>Numbers</h1>
<b>Ranges of Int:</b></br>  
- int (32 bit): -2x10^9~2x10^9</br>  
- Long long int(64 bit): -9x10^18~9x10^18</br>  

<b>Given:</b>  
❌int a=123456789;  
long long b = a * a;  
✔long a = 123456789;  
long long b = a * a;  
✔int a=123456789;  
long long b = (long long) a * a;  
