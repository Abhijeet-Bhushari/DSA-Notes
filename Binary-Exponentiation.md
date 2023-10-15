# Binary Exponentiation
Calculation of powers of large Exponent values within log(n) time constraint is possible through Binary Exponentiation.

Example: 

        					2^100
				           /     \
			           2^50       2^50
			          /    \     /    \
			      2^25	
			     /	  \
     		 2^12      2^12 * 2

The Algorithm will calculate the power in O(log(N)) Time complexity.

Code: 
```
int power(int x, long long n){
	if(n == 1) return x;
	if(n == 0) return 1;
	long long a = power(x, n/2) % Mod;
	a = (a * a) % Mod;
	if(n&1) a = (a * x) % Mod;
	return a;
}
```