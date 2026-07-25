```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {

 int t;
 cin>>t;
 while(t--){
     long long int n,q,l,r;
     cin>>n>>q;
     vector <int> a(n),b(n);
     for(auto &h:a){
     cin>>h;
     }
     for(auto &g:b)
     cin>>g;
  
       for(int i=0;i<n;i++){
       if(a[i]<b[i])
       a[i]=b[i];
            
        }
while(q--){
     cin>>l>>r;
        int sum=0;
       for(int i=l-1;i<r;i++)
       sum+=a[i];
       cout<<sum<<" ";
   } 
cout<<endl;
 }
}
```


