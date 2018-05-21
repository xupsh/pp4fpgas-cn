# pp4fpga-cn
Parallel Programming for FPGAs 中译版

Ryan Kastner, Janarbek Matai, and Stephen Neuendorffer

An open-source high-level synthesis book

http://hls.ucsd.edu/

## 写在前面
国内鲜有介绍HLS的书，我们希望通过翻译Parallel Programming for FPGAs这本书，让更多的人来了解HLS和FPGA开发。

## 翻译之前
Parallel Programming for FPGAs这本书的原作采用的是`latex`进行内容的编写和排版。为了提高翻译写作的速度和协作的效率，本次翻译任务选择了在`GitHub`这个平台上进行协作，采用了`Markdown`使得译者可以专注文字内容而不是排版样式，安心写作。

这也给参与翻译任务的诸位带来了一点小挑战，需要诸位事先熟悉一下`GitHub`平台的使用、`git`的使用以及`Markdown`语言的规范，下面是相关的参考链接给诸位快速上手。

### `Markdown`语言
> 事实上这篇README就是用Markdown写成的:)

[认识与入门Markdown](https://sspai.com/post/25137)

[Markdown 语法说明 (简体中文版)](http://wowubuntu.com/markdown/basic.html)

#### 引用图片的小技巧
```markdown
![images/2pointFFT.jpg](images/2pointFFT.jpg)
```
![images/2pointFFT.jpg](images/2pointFFT.jpg)

#### 引用代码的方式
>   只需要在代码片段前后都加上```符号，markdown就会自动将代码片段高亮出来

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

### `git`
git可以说是现在最为流行的版本管理工具了。

[廖雪峰的git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

[猴子都能懂的GIT入门](https://backlog.com/git-tutorial/cn/)

#### 常用命令
其实最常用的命令无非下面几条
##### 下载git库到本地
```
git clone https://github.com/xupsh/pp4fpgas-cn.git
```
##### 保存本地的修改并上传到云端服务器(GitHub)
```
git add -A
git commit -m "this should be your commit message"
git pull
git push
```

### `GitHub`的Pull Request操作
在`GitHub`上进行协作，通常采用的方式是先各自fork一份到自己的个人帐户，经过一段时间的工作之后，通过pull request的方式，将自己的工作内容提交到公共项目帐户中，而pull request之后往往还需要进行review才能正式进入公共项目。

[github的官方pull request文档](https://help.github.com/articles/about-pull-requests/)
#### Pull Request 的流程
-   第一步，你需要把别人的代码，克隆到你自己的仓库，Github 的术语叫做 fork。

-   第二步，在你仓库的修改后的分支上，按下"New pull request"按钮。

![new pr](http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071802.png)

-   这时，会进入一个新页面，有Base 和 Head 两个选项。Base 是你希望提交变更的目标，Head 是目前包含你的变更的那个分支或仓库。

![compare changes](http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071806.png)

-   第三步，填写说明，帮助别人理解你的提交，然后按下"create pull request"按钮即可。

-   PR 创建后，管理者就要决定是否接受该 PR。对于非代码变更（比如文档），单单使用 Web 界面就足够了。但是，对于代码变更，Web 界面可能不够用，需要命令行验证是否可以运行。

## 任务分工
|章节|译者|校对|
|-----|-----|-----|
|01 Introduction|||
|02 Finite Impulse Response(FIR) Filters|||
|03 CORDIC|||
|04 Discrete Fourier Transform|||
|05 Fast Fourier Transform|||
|06 Sparse Matrix Vector Multiplication|||
|07 Matrix Multiplication|||
|08 Prefix Sum and Histogram|||
|09 Video System|||
|10 Sorting Algorithms|||
|11 Huffman Encoding|||

## Citation
```
@ARTICLE{
    2018arXiv180503648K,
    author = {{Kastner}, R. and {Matai}, J. and {Neuendorffer}, S.},
    title = "{Parallel Programming for FPGAs}",
    journal = {ArXiv e-prints},
    archivePrefix = "arXiv",
    eprint = {1805.03648},
    keywords = {Computer Science - Hardware Architecture},
    year = 2018,
    month = may
}
```