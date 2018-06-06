# pp4fpga-cn

中文版 `Parallel Programming for FPGAs`

电子书阅读地址: [https://xupsh.github.io/pp4fpgas-cn](https://xupsh.github.io/pp4fpgas-cn)

电子书下载地址: [pdf]()

## 写在前面
国内鲜有介绍HLS的书，我们希望通过翻译Parallel Programming for FPGAs这本书，让更多的人来了解HLS和FPGA开发。

## 翻译之前
Parallel Programming for FPGAs这本书的原作采用的是`latex`进行内容的编写和排版。为了提高翻译写作的速度和协作的效率，本次翻译任务选择了在`GitHub`这个平台上进行协作，采用了`Markdown`使得译者可以专注文字内容而不是排版样式，安心写作。

这也给参与翻译任务的诸位带来了一点小挑战，需要诸位事先熟悉一下`GitHub`平台的使用、`git`的使用以及`Markdown`语言的规范，下面是相关的参考链接给诸位快速上手。

### 翻译规范
- [翻译规范](RULES.md)

### 编辑器
一个界面美观、交互UI设计良好的编辑器可以帮我们节省很多力气，这里我们比较推荐使用以下几款编辑器来进行翻译工作
- [Atom](https://atom.io/)
- [VS Code](https://code.visualstudio.com/)

### `Markdown`语言
> 事实上这篇README就是用Markdown写成的 :)

- [认识与入门Markdown](https://sspai.com/post/25137)
- [Markdown 语法说明 (简体中文版)](http://wowubuntu.com/markdown/basic.html)

### `git`
git可以说是现在最为流行的版本管理工具了。

- [廖雪峰的git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)
- [猴子都能懂的GIT入门](https://backlog.com/git-tutorial/cn/)

其实最常用的命令无非下面几条
##### 下载git库到本地
```console
git clone https://github.com/xupsh/pp4fpgas-cn.git
```
##### 保存本地的修改并上传到云端服务器(GitHub)
```console
git add -A
git commit -m "最近的修改里都做了什么"
git pull
git push
```

### `GitHub`的Pull Request操作
在`GitHub`上进行协作，通常采用的方式是先各自fork一份到自己的个人帐户，经过一段时间的工作之后，通过pull request的方式，将自己的工作内容提交到公共项目帐户中，而pull request之后往往还需要进行review才能正式进入公共项目。

[github的pull request官方文档](https://help.github.com/articles/about-pull-requests/)
#### Pull Request 的流程
-   第一步，你需要把别人的代码，克隆到你自己的仓库，Github 的术语叫做 fork。

-   第二步，在你仓库的修改后的分支上，按下"New pull request"按钮。

![new pr](http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071802.png)

-   这时，会进入一个新页面，有Base 和 Head 两个选项。Base 是你希望提交变更的目标，Head 是目前包含你的变更的那个分支或仓库。

![compare changes](http://www.ruanyifeng.com/blogimg/asset/2017/bg2017071806.png)

-   第三步，填写说明，帮助别人理解你的提交，然后按下"create pull request"按钮即可。

-   PR 创建后，管理者就要决定是否接受该 PR。对于非代码变更（比如文档），单单使用 Web 界面就足够了。但是，对于代码变更，Web 界面可能不够用，需要命令行验证是否可以运行。

## 任务分工
[见Wiki页面](https://github.com/xupsh/pp4fpgas-cn/wiki#%E4%BB%BB%E5%8A%A1%E5%88%86%E5%B7%A5)
## Citation
[https://github.com/KastnerRG/pp4fpgas](https://github.com/KastnerRG/pp4fpgas)
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
