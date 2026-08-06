
##
```cpp
auto it = max_element(mp.begin(), mp.end(),
        [](const auto &a, const auto &b) {
            return a.second < b.second;
        });
##
  int sum = accumulate(mp.begin(), mp.end(), 0,
        [](int s, const auto &p) {
            return s + p.second;
        });
##
Sort by value (descending)
sort(v.begin(), v.end(), [](auto &a, auto &b) {
    return a.second > b.second;
});
##

##
