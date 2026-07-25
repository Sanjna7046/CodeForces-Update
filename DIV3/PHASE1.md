
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
int n;

cin>>n;

while(n--){
  int t,maxa=0,count=0;
   cin>>t;
  vector<int> arr(t);
  for(auto &x:arr){
      cin>>x;
      if(x==maxa)count++;
      else if(x>maxa){
      maxa=x;
      count=1;}
  }
  cout<<count<<endl;
        

}

}``
