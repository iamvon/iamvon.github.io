---
layout: post
title: Thuật toán sinh chuỗi kí tự ngẫu nhiên
tags: [chuyencoding]
description: >
  Test code highlight.
author: von
comments: yes
---
Đoạn code C++ sinh 1 chuỗi ký tự ngẫu nhiên:

```cpp
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

static const char chuoikytu [] =
"0123456789"
"abcdefghijklmnopqrstuvwxyz"
"ABCDEFGHIJKLMNOPQRSTUVWXYZ"
"!@#$%^&/?()_-+;:.|~×÷`" ;

int size = sizeof(chuoikytu) - 1;

int main()
{
    int length = 8;
    srand(time(0));
    for (int i = 0; i < length; i++)
    {
        cout << chuoikytu [rand() % size];
    }
    return 0;
}

```
