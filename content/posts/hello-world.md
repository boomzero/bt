+++
title = "test"
date = "2023-02-10T11:21:34+08:00"
author = ""
authorTwitter = "" #do not include @
cover = ""
tags = ["", ""]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = false
hideComments = false
color = "" #color from the theme settings
+++
# this is a test
now here is some sorce code:
```cpp
#include <bits/stdc++.h>

using namespace std;
int c[105] = {0}, w[105] = {0};

int f(int i, int v) {
    if (i == 0 || v == 0) return 0;
    if (v < c[i]) {
        return f(i - 1, v);
    }
    return max(f(i - 1, v), f(i - 1, v - c[i]) + w[i]);
}

int main() {
    int v, n;
    cin >> v >> n;
    for (int i = 1; i <= n; ++i) {
        scanf("%d%d", &c[i], &w[i]); // NOLINT(cert-err34-c)
    }
    cout << f(n, v) << endl;
    return 0;
}
```
