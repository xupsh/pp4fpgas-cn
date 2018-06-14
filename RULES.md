# 排版约定

## 引用公式
使用示例:

![](images/katex.png)

Inline math: $\int_{-\infty}^\infty g(x) dx$

Block math:

$$
\int_{-\infty}^\infty g(x) dx \quad (4.1)
$$

## 引用代码
只要将代码用```包住，代码块就会被识别为代码
````
```c
#include "huffman.h"
// Postcondition: out[x].frequency > 0
void filter(
            /* input  */ Symbol in[INPUT_SYMBOL_SIZE],
            /* output */ Symbol out[INPUT_SYMBOL_SIZE],
            /* output */ int *n) {
#pragma HLS INLINE off
    ap_uint<SYMBOL_BITS> j = 0;
    for(int i = 0; i < INPUT_SYMBOL_SIZE; i++) {
#pragma HLS pipeline II=1
        if(in[i].frequency != 0) {
            out[j].frequency = in[i].frequency;
            out[j].value = in[i].value;
            j++;
        }
    }
    *n = j;
}
```
````

```c
#include "huffman.h"
// Postcondition: out[x].frequency > 0
void filter(
            /* input  */ Symbol in[INPUT_SYMBOL_SIZE],
            /* output */ Symbol out[INPUT_SYMBOL_SIZE],
            /* output */ int *n) {
#pragma HLS INLINE off
    ap_uint<SYMBOL_BITS> j = 0;
    for(int i = 0; i < INPUT_SYMBOL_SIZE; i++) {
#pragma HLS pipeline II=1
        if(in[i].frequency != 0) {
            out[j].frequency = in[i].frequency;
            out[j].value = in[i].value;
            j++;
        }
    }
    *n = j;
}
```

## 引用图片
在行文中使用下述格式引用图片，将图片下方的备注写在`[]`之间
```markdown
![Figure 5.1: Part a) is a data flow graph for a 2 point DFT/FFT. Part b) shows the same compu-tation, but viewed as a butterfly structure. This is a common representation for the computation of an FFT in the digital signal processing domain.](images/2pointFFT.jpg)
```

![Figure 5.1: Part a) is a data flow graph for a 2 point DFT/FFT. Part b) shows the same compu-tation, but viewed as a butterfly structure. This is a common representation for the computation of an FFT in the digital signal processing domain.](images/2pointFFT.jpg)

## 文字加框
### 原书中蓝色的框
```
{% hint style='info' %}
Important info: this note needs to be highlighted
{% endhint %}
```
{% hint style='info' %}
Important info: this note needs to be highlighted
{% endhint %}
### 原书中黑色的框
```
{% hint style='tip' %}
Important tip: this note needs to be highlighted
{% endhint %}
```
{% hint style='tip' %}
Important tip: this note needs to be highlighted
{% endhint %}
### 其它 请酌情使用
```
{% hint style='danger' %}
Important danger: this note needs to be highlighted
{% endhint %}
```
{% hint style='danger' %}
Important danger: this note needs to be highlighted
{% endhint %}
```
{% hint style='working' %}
Important working: this note needs to be highlighted
{% endhint %}
```
{% hint style='working' %}
Important working: this note needs to be highlighted
{% endhint %}

## 引用参考文献
在行文中使用下述格式引用参考文献即可
```
[[45](./BIBLIOGRAPHY.md#45), [55](./BIBLIOGRAPHY.md#55)]
```
[[45](./BIBLIOGRAPHY.md#45), [55](./BIBLIOGRAPHY.md#55)]
