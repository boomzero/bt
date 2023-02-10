---
title: "Intro"
date: 2023-02-10
thumbnailImagePosition: left
thumbnailImage: //d1u9biwaxjngwg.cloudfront.net/cover-image-showcase/city-750.jpg
---
# union-find set
```cpp
int T, N, M, id[1010], sz[1010], ans;

int find(int x) {
    if (id[x] == x) return x;
    return id[x] = find(id[x]);
}

void join(int x, int y) {
    int p = find(x);
    int q = find(y);
    if (p != q) {
        id[p] = q;
        sz[q] += sz[p];
    }
}
```

