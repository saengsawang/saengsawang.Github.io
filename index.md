## Welcome To My Interview Experience

本网站用于记录作者从大三暑假找实习开始经历过的所有笔试和面试题。包括以下公司：Oasis（绿洲VR）、字节跳动、Ubisoft···

### Oasis   —— 2020/06/16

Oasis是一个15-50人的小公司，在上海交大徐汇校区旁边，在开发“绿洲VR”的虚拟世界社交网络平台。没有现场的笔试和面试，只是技术负责人打电话沟通了一下项目经历等，然后给了两道笔试题要求在两天之内给出解决思路。

```markdown
这两道笔试题具体要求如下：

# VRIK

- 背景
1. 我们基于**Unity HumanBodyBones**这个枚举来同步⼈体数据；
2. 我们的⼈体3D模型均来⾃⽤户上传，⼈体各部分⽐例千差万别。

- 问题
我们期望在HumanBodyBones输⼊数据相同的情况下，在⼈体各部分⽐例不同的3D模型上输出⼀致的动作。
请问如何着⼿解决这个技术问题?

- 思路
1. 在用户上传3D模型时，规定用户需自己选定关键的关节节点，如肩膀、 手肘、手腕、手脚指头、颈部、胯部、膝盖和脚踝等。 
**In Details**：在用户层面，要求用户在上传模型后需要对模型进行一些fix操作，
                保留末端骨骼和连接骨骼这两步就可以完成对模型关键节点的定义。
                考虑到用户友好性，把整个需要用户自行在Unity引擎中操作的步骤封装成一个API，
                然后在游戏中每次用户选择自行上传模型时就调用之，
                而后在模型创建界面用可视化的界面让用户对其进行交互操作，定义关节。
**Pros And Cons**：操作较为简单，宜于代码实现。
                而且对于一些不具备常见骨骼形体的非人体模型的来说，也算是 一种较为通用的解决方法。
                目前已经较多地应用于 Unity 制作的多款可以提供用户自行上传模型机会的游戏中（譬如 VRchat）
                
# 通信协议

- 背景
1. 我们客户端之间是类似点对点式的通信模式，服务端只负责转发/⼴播，客户端⾃⼰负责通信协议的封包与解包；
2. 未来我们会在类似steam、epic等多个游戏平台同时上线我们的产品，势必造成客户端与客户端之间的通信协议版本不⼀致。

- 问题
如果两个使⽤不同版本通信协议的客户端需要相互通信时，有可能造成数据解析错误，
请问如果由你设计通信协议，你会怎样做来尽可能规避数据解析错误呢？
提示：可以参考 P2P 通信协议。
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/saengsawang/saengsawang.Github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
