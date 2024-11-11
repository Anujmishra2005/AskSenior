```
#include <iostream>
#include <vector>
using namespace std;

int main() {
    int N, Q;
    cin >> N >> Q;
    
    vector<long long> A(N + 1), prefix(N + 1, 0);
    
    // Read the array A (1-based indexing)
    for (int i = 1; i <= N; i++) {
        cin >> A[i];
    }
    
    // Construct prefix sum array
    for (int i = 1; i <= N; i++) {
        prefix[i] = prefix[i - 1] + A[i];
    }
    
    // Answer each query
    while (Q--) {
        int L, R;
        cin >> L >> R;
        cout << prefix[R] - prefix[L - 1] << endl;
    }

    return 0;
}

```
