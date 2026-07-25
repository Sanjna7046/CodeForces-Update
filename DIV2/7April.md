```cpp
#include <bits/stdc++.h>
using namespace std;

int countt(vector<int>& ind, vector<int>& v){
    vector<int> ghi;

    for(int j = 0; j < ind.size(); j++){
        int col = 0, cor = 0;

        int ink = ind[j] - 1;   // FIXED (1-based → 0-based)
        int m = v[ink];

        // LEFT side
        for(int i = 0; i < ink; ){
            if(v[i] != m){
                col++;
                while(i < ink && v[i] != m) i++;
            } else i++;
        }

        // RIGHT side
        for(int i = ink + 1; i < v.size(); ){
            if(v[i] != m){
                cor++;
                while(i < v.size() && v[i] != m) i++;
            } else i++;
        }

        ghi.push_back(max(cor, col));
    }

    return *min_element(ghi.begin(), ghi.end());
}

int main() {
    ios::sync_with_stdio(false);
    cin.tie(NULL);

    int t;
    cin >> t;

    while(t--){
        int n, k;
        cin >> n >> k;

        vector<int> v(n);
        for(int i = 0; i < n; i++){
            cin >> v[i];
        }

        vector<int> in(k);
        for(int i = 0; i < k; i++){
            cin >> in[i];
        }

        int co = countt(in, v);

        cout << 2 * co << "\n";
    }
}
```
```cpp

#include <bits/stdc++.h>
using namespace std;

int countt(int m,int ind,vector <int> v){
    int col=0,cor=0;
    for(int i=0;i<ind-1;){
        if(v[i]!=m){ col++;
        while(i<ind-1&&v[i]!=m)i++;}
        else i++;
    }
    for(int i=ind;i<v.size();){
        if(v[i]!=m){ cor++;
        while(i<v.size()&&v[i]!=m)i++;}
        else i++;
    }
    return 2*max(cor,col);
}
int main() {
	// your code goes here
int t;
cin>>t;
while(t--){
 int n,k,co=0;
    cin>>n>>k;
    vector <int> v(n);
    for(int i=0;i<n;i++){
        cin>>v[i];
    
        
    }
   int in;
   cin>>in;
   
       co=countt(v[in-1],in,v);
 
   cout<<co<<endl;
}
}
```
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
	// your code goes here
int t;
cin>>t;
while(t--){
 int n,k,sum=0;
    cin>>n>>k;
    vector <int> v(n);
    for(int i=0;i<n;i++){
        cin>>v[i];
    sum+=v[i];
        
    }
    if(sum%2!=0){
        cout<<"YES"<<endl;
    
    }
    else if((k*n)%2==0)   cout<<"YES"<<endl;
    else   cout<<"NO"<<endl;
}
}
```
