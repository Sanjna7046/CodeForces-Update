
## 1
```cpp
#include <bits/stdc++.h>

using namespace std;

int main() {
        int t;
        cin >> t;
        while (t--) {
            int n;
            cin >> n;
         vector<int> v;
         int sum=0;
        map<int,int> mp;
         
             int k;
         for(int i=0;i<n;i++){
             cin>>k;
             v[i]==k;
            mp[k]++;
            sum+=k;
            }
           int ct=0;
       for(auto &p : mp){
           ct=max(ct,p.second);
       }
        if(n>=2*(ct)-2)
    {
        cout<<sum;
    }
    else{
       int summ=0;
       for(auto &pp:mp){
           if(pp.second!=ct){
               summ+=pp.first*pp.second;
               
           }
           else 
           summ+=pp.first*(n-pp.second+2);
       }
       cout<<summ;
           }
    
    cout<<endl;
        }
}

```
## 2
```cpp
#include <bits/stdc++.h>
 using namespace std;
 int main() {
 int t;
cin >> t;
 while (t--) {
int n;
 int odd=0,even=0;
cin >> n;
 string s;
cin>>s;
vector<int> v(n);
 for(int i=0;i<n;i++){
 v[i]=s[i]-'0';
 if(v[i]==1)odd++;
else even++;
 }
int e0=0,o1=0;
 for(int i=0;i<n-1;i++){
if(v[i]==v[i+1]){
if(v[i]==1)o1++;
else e0++;
 }
 }
 if(abs(e0-o1)<2)
cout<<e0+o1;
 else if((e0>o1&&e0<=odd+1)||(o1>e0&&o1<=even+1))
 cout<<2*(e0>o1?e0:o1)-1;
else cout<<-1;
cout<<endl;
 }
}
```
