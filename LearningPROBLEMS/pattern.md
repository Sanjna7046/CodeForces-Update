
# 1.
```cpp
*      *
**    **
***  ***
********
***  ***
**    **
*      *
```
## my approach
```cpp
 for (int j = 0; j < 2 * n-1; j++) {
        int k = min(j + 1, 2 * n - j - 1);
        for (int h = 0; h < k; h++) {
            cout << '*';

        }
        for (int g = k; g < n; g++) {
            cout << " ";
        }
        for (int g = k; g < n; g++) {
            cout << " ";
        }
        for (int h = 0; h < k; h++) {
            cout << '*';

        }


        cout << endl;
    }
```
## better approach
```cpp
 for (int j = 0; j < 2 * n-1; j++) {
        int k = min(j + 1, 2 * n - j - 1);
          cout << string(k, '*')
             << string(2 * (n - k), ' ')
             << string(k, '*');


        cout << endl;
    }
```


