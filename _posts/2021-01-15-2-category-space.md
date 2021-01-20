---
layout: post
title:  "카테고리에 띄어쓰기 넣는 방법"
description: 카테고리 섹션에 띄어쓰기 넣는 방법
date:   2021-01-15 17:00:00 +0900
categories: 
  - Blog
---
지난 Post를 작성하던 도중 카테고리에 Windows Terminal을 넣고 싶었다. 
그러나 각 카테고리를 띄어쓰기로 구분하고 있었기에 단순하게 쌍 따옴표로 묶어주면 된다고 생각했다.

```
categories: Bash Vim "Windows Terminal"
```
하지만 결과는 아래와 같았다.

![NoApplySpace](https://github.com/zdevowl/zdevowl.github.io/blob/master/_posts/2021-01-15-2-category-space-pic-1.JPG?raw=true)

검색을해봐도 잘 나오지 않다가 누군가 아래와 같은 방식으로 적은 것을 보았다.
```
categories: 
    - Bash 
    - Vim 
    - Windows Terminal
```

이제 원하는대로 나온다.

![ApplySpace](https://github.com/zdevowl/zdevowl.github.io/blob/master/_posts/2021-01-15-2-category-space-pic-2.JPG?raw=true)

