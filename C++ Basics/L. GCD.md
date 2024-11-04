```
#include<bits/stdc++.h>
using namespace std;
 
int gcd(int a , int b)
{
    if (a == 0)
    {
        return b;
    }
    return gcd(b%a,a);
}
 
int main()
{
    int a,b;
    cin >> a >> b;
    if (a>b)
    {
        swap(a,b);
    }
    int ans1 = gcd(a,b);
    cout << ans1 << endl;
    int ans = gcd(a,b);
}
```
