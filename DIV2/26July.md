```cpp
#include <bits/stdc++.h>

using namespace std;
string solve(int n, int k){
    string s;
     for(int i=0;i<n/2;i++) s.push_back('1');
        for(int i=0;i<(n+1)/2;i++) s.push_back('0');
        return s;
}

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n,k;
        cin >> n>>k;
       string s;
       if(n-k==1)
       cout<<"-1";
       else if(n==k+2){
       s=solve(n,k); 
       cout<<s;
       }
       else{
           s=solve(k+2,k);
           for(int i=0;i<n-k-2;i++){
               if(i%2==0)
               s.push_back('1');
               else 
               s.push_back('0');
           }
               cout<<s;
       }
        cout << endl;
    }

}
```
```cpp

#include <bits/stdc++.h>

using namespace std;

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        cin >> n;
        vector < int > v(n);
        for (int i = 0; i < n; i++) {
            cin >> v[i];
        }
        if (n == 1 || n % 2 != 0)
            cout << "NO";
        else {

            bool kk = true;
            for (int i = 0; i < n-1; i++) {
                if (v[i] > v[i+1] + 1) { i++;
                continue;
                }
                else {
                    cout << "NO";
                    kk = false;
                    break;
                }





            }
            if (kk) {
                sort(v.begin(), v.end());
                if (v[n / 2] > v[(n - 1) / 2] + 1)
                    cout << "YES";
                    else
                    cout<<"NO";
            }

        }

        cout << endl;
    }

}

```
