```
#include <iostream>
using namespace std;

int main() {
    int N, M, X;
    cin >> N >> M;
    
    bool found = false;
    int element;

    for (int i = 0; i < N; ++i) {
        for (int j = 0; j < M; ++j) {
            cin >> element;
            if (element == X) {
                found = true;
            }
        }
    }

    cin >> X;

    if (found) {
        cout << "will not take number" << endl;
    } else {
        cout << "will take number" << endl;
    }

    return 0;
}

```
