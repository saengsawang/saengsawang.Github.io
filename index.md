## Welcome To My Interview Experience

本网站用于记录作者从大三暑假找实习开始经历过的所有笔试和面试题。包括以下公司：Oasis（绿洲VR）、字节跳动、Ubisoft···

### Oasis ——2020/06/16

Oasis是一个15-50人的小公司，在上海交大徐汇校区旁边，在开发“绿洲VR”的虚拟世界社交网络平台。没有现场的笔试和面试，只是技术负责人打电话沟通了一下项目经历等，然后给了两道笔试题要求在两天之内给出解决思路。

```markdown
这两道笔试题具体要求如下：

# VRIK
- 背景
1. 我们基于*Unity HumanBodyBones*这个枚举来同步⼈体数据；
2. 我们的⼈体3D模型均来⾃⽤户上传，⼈体各部分⽐例千差万别。
- 问题
我们期望在HumanBodyBones输⼊数据相同的情况下，在⼈体各部分⽐例不同的3D模型上输出⼀致的动作。请问如何着⼿解决这个技术问题？
- 思路
1. 在用户上传3D模型时，规定用户需自己选定关键的关节节点，譬如：肩膀、 手肘、手腕、手脚指头、颈部、胯部、膝盖和脚踝等（主要就是一些会涉及到虚拟角色运动 的关节）。 
In Details：在用户层面，要求用户在上传模型后需要对模型进行一些fix操作，其中，保留末端骨骼和连接骨骼这两步就可以完成对模型关键节点的定义。考虑到用户友好性，把整个需要用户自行在Unity引擎中操作的步骤封装成一个API，然后在游戏中每次用户选择自行上传模型时就调用之，而后在模型创建界面用可视化的界面让用户对其进行交互操作，定义关节。
Pros And Cons：这种让用户在上传模型时就
## Header 2
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
