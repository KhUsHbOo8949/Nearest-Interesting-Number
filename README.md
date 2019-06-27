# Nearest-Interesting-Number
Polycarp knows that if the sum of the digits of a number is divisible by 3, then the number itself is divisible by 3. He assumes that the numbers, the sum of the digits of which is divisible by 4, are also somewhat interesting. Thus, he considers a positive integer n interesting if its sum of digits is divisible by 4.  Help Polycarp find the nearest larger or equal interesting number for the given number a. That is, find the interesting number n such that n≥a and n is minimal.  Input The only line in the input contains an integer a (1≤a≤1000).  Output Print the nearest greater or equal interesting number for the given number a. In other words, print the interesting number n such that n≥a and n is minimal.  








#include <bits/stdc++.h>
using namespace std;
int sum(int x)
{
    int sum=0;
    while(x!=0)
    {
        sum+=x%10;
        x=x/10;
    }
    return sum;
}

int main() 
{  
	int a;
	cin>>a;
	while(a<=10000)
	{
	int n,z;
	n=sum(a);
	if(n%4==0)
	break;
	else
	a++;
	}
	cout<<a<<"\n";
	return 0;
}
