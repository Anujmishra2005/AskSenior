```
#include<bits/stdc++.h>
using namespace std;

int main()
{
    int n;
    cin >> n;
    string A;
    cin >> A;

    int digit_sum = 0;

    for(int i=0; i<n ; i++)
    {
        digit_sum += A[i] - '0';
    }
    cout << digit_sum << endl;
}

```
