```
#include <iostream>
#include <vector>
using namespace std;

int countNonDecreasingSubarrays(const vector<int>& A, int N) {
    int count = 0, length = 1;
    for (int i = 1; i < N; ++i) {
        if (A[i] >= A[i - 1]) {
            length++;
        } else {
            count += (length * (length + 1)) / 2;
            length = 1;
        }
    }
    count += (length * (length + 1)) / 2;
    return count;
}

int main() {
    int T;
    cin >> T;
    while (T--) {
        int N;
        cin >> N;
        vector<int> A(N);
        for (int i = 0; i < N; ++i) cin >> A[i];
        cout << countNonDecreasingSubarrays(A, N) << endl;
    }
    return 0;
}

```
