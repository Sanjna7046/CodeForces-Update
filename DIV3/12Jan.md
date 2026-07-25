```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
    int t;
    cin>>t;
    while(t--){
       int n;
       cin>>n;
       if(n==2||n==3)
       cout<<n<<endl;
   
       else if(n%2==0)
       cout<<0<<endl;
       else
       cout<<1<<endl;
  
    }
}
}
```
```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
    int t;
    cin>>t;
    while(t--){
       long long int s,k,m,p;
       cin>>s>>k>>m;
       while(m/k>=1){
           if(s>k)
           s=k;
           m=m-k;
       }
      p= s-abs(m%k);
        if(p<0)
        cout<<0<<endl;
        else 
        cout<<p<<endl;
    }
}
```
