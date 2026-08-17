
```cpp
#include <bits/stdc++.h>

using namespace std;

int main() {
    int t;
    cin >> t;

    while (t--) {
        int n, m;
        cin >> n >> m;
        map < char, int > mp;
       
        while(n--) {
            string k;
            cin >> k;
            mp[k[0] - 'a' + 'A']++;
        }
        bool hh = false;
       while(m--) {
           string p;
            cin >> p;
            for (auto & c: p) {
                if (mp[c] == 0&& !hh) {
                    cout << "no" << endl;
                    hh = true;
                    break;
                }

            }
            mp[p[0]]++;
        }
        if (!hh)
            cout << "yes" << endl;


    }

}
```
