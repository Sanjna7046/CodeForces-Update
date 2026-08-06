## 1
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
int t;
cin>>t;
while(t--){
   vector<int> v(3);
   for(auto &k:v){
       cin>>k;
   }
   int count=0;
   std::sort(v.begin(), v.end());
 while(! (v[0]==v[1]||v[2]==v[1]||v[0]==v[2])){
      v[0]++;
      v[2]--;
      std::sort(v.begin(), v.end());
       count++;
   }
   cout<<count<<endl;
}
}
```
## 2
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
int t;
cin>>t;
while(t--){
   int n;
   cin>>n;
   string s;
   cin>>s;
  
  
   int count=0,countt=0;
   for(int i=1;i<s.size()-1;i++){
       if(s[i-1]==s[i+1]&&s[i]!=s[i+1]){
           count++;
           auto it = s.begin();
advance(it, i);

s.erase(it);
           break;
       }
   }
   if(!count){
     auto it2 = s.begin();
advance(it2, n/2);

s.erase(it2);
}
n=s.size();
for(int i=0;i<n-1;i++){
    if(s[i]==s[i+1]){
        if(s[i]!=s[i+2]&&(i+2<n)){
            countt++;
            i++;
        }
        else
        i++;
    }
    else
    countt++;
}
   cout<<countt+1<<endl;
}
}
```
### mine cause TLE , so CF wala answer 
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int t;
    cin >> t;

    while (t--) {
        int n;
        cin >> n;

        string s;
        cin >> s;

        int groups = 1;
        for (int i = 1; i < n; i++)
            if (s[i] != s[i - 1])
                groups++;

        int ans = INT_MAX;

        for (int i = 1; i < n - 1; i++) {
            int left  = (s[i] != s[i - 1]);
            int right = (s[i] != s[i + 1]);
            int after = (s[i - 1] != s[i + 1]);

            int cur = groups - (left + right) + after;
            ans = min(ans, cur);
        }

        cout << ans << '\n';
    }

    return 0;
}

```
## 3a
```cpp
https://codeforces.com/blog/entry/155666
```
## 3b
```cpp

```
