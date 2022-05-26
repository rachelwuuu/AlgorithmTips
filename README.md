# AlgorithmTips
Disclaimer: The following notes are taken from the book "Competitive Programmer's Handbook"
<h1>Numbers</h1>
Ranges of Int:
- int (32 bit): -2x10^9~2x10^9
- Long long int(64 bit): -9x10^18~9x10^18

Given:
❌int a=123456789; \n
long long b = a * a; \n
✔long a = 123456789;\n
long long b = a * a;\n
✔int a=123456789;\n
long long b = (long long) a * a;
