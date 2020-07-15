## Welcome To My Interview Experience

本网站用于记录作者从大三暑假找实习开始经历过的所有笔试和面试题。包括以下公司：Oasis（绿洲VR）、字节跳动、Ubisoft···

### Oasis（游戏开发实习生）   —— 2020/06/16

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
                
2. 运用深度学习的方法，通过事先上传大量不同比例的模型来训练网络，在用户自己上传模型后可以通过模型的形状识别出可活动的关节等信息。
**Pros And Cons**：代码工程量巨大，不好实现，现阶段相对第一种方法来说耗时耗力而且效果不一定令人满意。
                但可以结合第一种方法对第二种方法做一定的改进，主要就是用户上传模型后先运用第二种深度学习的方法识别节点，
                若节点都正确则继续下一步，若是有的节点不正确再调用第一种方法对节点进行可交互的调整。
                
                
# 通信协议


- 背景
1. 我们客户端之间是类似点对点式的通信模式，服务端只负责转发/⼴播，客户端⾃⼰负责通信协议的封包与解包；
2. 未来我们会在类似steam、epic等多个游戏平台同时上线我们的产品，势必造成客户端与客户端之间的通信协议版本不⼀致。

- 问题
如果两个使⽤不同版本通信协议的客户端需要相互通信时，有可能造成数据解析错误，
请问如果由你设计通信协议，你会怎样做来尽可能规避数据解析错误呢？
提示：可以参考 P2P 通信协议。

- 思路
**Suppose**：A和B具有不同版本的通信协议，但需要通信，如何规避数据解析错误？ 
1. A 和 B 在通信传输之前事先交换协议栈。 
2. 编写一个第三方 M，同时兼容A和B的通信协议，并且可以在其上对不同版 本的通信协议进行互相的转换和解读。（A to M, M to B） 
**Pros And Cons**：第一种方法因为是直接交换协议栈，明显会快于第二种方法，交换IP地址而后再进行一些操作便可以实现正确的通信传输。
                   而第二种方法系统的鲁棒性会更高，如果有第三个用户C想要加入AB之间通信的话，就只需使M兼容C的通信协议并且可以转换解读，
                   这样无论多少个用户想加入传输都可以，应用范围较为广泛。（A,B,C to M; M to A,B,C）

```

### Ubisoft（HR Information System Analyst Intern）   —— 2020/06/22

育碧投的这个岗位，当时理解的是做前端后端，结果发现其实是要做一个完整的系统，当时我是啥都不会（现在也是），因此没有通过，暂且记录下来。

```markdown
限时四十分钟：


1. A business man has bought a farm by the sea and developed a new campsite containing onsite caravans and tent pitches which can be booked. 
Each caravan is given a unique number and description. Each tent pitch will also be uniquely numbered. 
He requires a new on-line system to deal with enquiries and bookings. 

Customers will log on and enter the required date and number of weeks indicating whether they wish to book a caravan or a tent pitch. 
The system will check and confirm if the required dates are available. 
If the dates are available, the customer will be asked if they wish to continue with the booking and to enter their personal details. 
The system will also require a deposit to be paid using a secure on-line payment system. 
When the deposit is received a confirmation invoice will be emailed to the customer detailing the outstanding payment which must be paid four weeks before the arrival date. 

a) List the external entities, processes and data stores in the above scenario and draw a high level logical data flow diagram. 
b) Identify the systems entities and relationships and draw an entity relationship diagram dealing with the booking process only. 
c) Briefly describe the role and skills of the following: 
  (i) System analyst/designer
  (ii) Programmer
  
  
2. a) What makes a good screen design? Discuss the techniques that can be used to assist the users. 
   b) Draft a series of on-line screens depicting the booking process in question A1, displaying available dates and indicate the validation of each field. 
   c) Describe the theory and main features of a relational database.
   
   
3. a) Discuss how a testing strategy should be prepared. Include various techniques which could be used and describe the difference between black and white box testing. 
   b) Briefly describe the advantages and disadvantages of the following: 
     i) Stage implementation 
     ii) Direct implementation 
     iii) Parallel implementation 
   c) Outline measures you would use to protect data from malicious and accidental loss/access.
   
4. What structures and procedures would you put in place to ensure that all documentation generated during a project was to the highest standard?

5. Without reference to cost or time, discuss the advantages and disadvantages of a prototyping technique of your choice.

6. Briefly describe the following methodologies: (i) Waterfall (5 marks) (ii) Object oriented (5 marks) (iii) Agile

```

### 字节跳动（后端开发工程师——视频架构）   —— 2020/06/28一面 2020/07/09二面

字节跳动投的不是日常实习生，而是秋招提前批，因此前前后后一共会有三次面试。一面通过了，很遗憾二面没通过。

```markdown
根据我模糊的记忆写下这两次面试的题目，一面由于第二道编程题写了好久所以是一个半小时，二面总共一个小时不到一点。


# 一面


- 基础知识
计算机网络：分层架构、TCP等
操作系统：进程调度方法
算法：各种排序的区别和实现
计算机安全：isa协议
数据结构：链表、红黑树原理以及与普通二叉树的区别
数据库：左连接右连接

- 编程
1. 判断一棵二叉树是否对称（镜像对称）

**Answer** 两个节点存储的值相等；
           节点A的左子树节点与节点B的右子树节点对称；
           节点A的右子树节点与节点B的左子树节点对称。
       
2.  多叉树（字典树）的查询插入

**Answer** 可以用数组实现，可以用链表，具体查百度（我也没写好）


# 二面


- 基础知识
1. Python为什么多[线程]运行速度比单线程的慢？
**Answer** GIL会锁定Python线程中的CPU执行资源，线程在执行代码时，要先获得这把锁才可以获得CPU的执行代码指令。
           如果锁被别的线程占用，该线程就只能等待直到锁被释放。
           [GIL是CPython解释器特有的全局解释器锁，在该解释器中线程要想执行CPU指令需要：
             （i）被操作系统调度出来（操作系统允许它占用CPU）
             （ii）获取到GIL（CPython解释器允许它执行指令）]
           解决方法：（i）使用多进程（进程之间没有GIL限制）
                    （ii）使用Jython，IronPython等没有GIL的解释器
                    （iii）使用协程（高效的单线程模式）

2. C++里虚函数的作用
**Answer** 实现多态性（Polymorphism），多态性是将接口与实现进行分离；
           通俗地说：实现以共同的方法，但因个体差异，而采用不同的策略。
           [注意虚函数和纯虚函数的区别]
         
3. HTTP状态码有哪些？301和302的区别？
**Answer** 1xx：代表请求已被接受，需要继续处理。这类响应是临时响应，只包含状态行和某些可选的响应头信息，并以空行结束。
           2xx：代表请求已成功被服务器接收、理解、并接受。
           3xx：代表需要客户端采取进一步的操作才能完成请求。
           4xx：代表客户端看起来可能发生了错误，妨碍了服务器的处理。
           5xx、6xx：代表服务器在处理请求的过程中有错误或者异常状态发生，也有可能是服务器意识到以当前的软硬件资源无法完成对请求的处理。
           
           301 Moved Permanently
           被请求的资源已永久移动到新位置，并且将来任何对此资源的引用都应该使用本响应返回的若干个 URI 之一。
           如果可能，拥有链接编辑功能的客户端应当自动把请求的地址修改为从服务器反馈回来的地址。除非额外指定，否则这个响应也是可缓存的。
           新的永久性的URI 应当在响应的 Location 域中返回。除非这是一个 HEAD 请求，否则响应的实体中应当包含指向新的 URI 的超链接及简短说明。
           如果这不是一个 GET 或者 HEAD 请求，因此浏览器禁止自动进行重定向，除非得到用户的确认，因为请求的条件可能因此发生变化。
           
           302 Move Temporarily
           请求的资源临时从不同的 URI响应请求。由于这样的重定向是临时的，客户端应当继续向原有地址发送以后的请求。
           只有在Cache-Control或Expires中进行了指定的情况下，这个响应才是可缓存的。
           上文有提及。
           如果这不是一个 GET 或者 HEAD 请求，那么浏览器禁止自动进行重定向，除非得到用户的确认，因为请求的条件可能因此发生变化。
           
4. 线程状态有什么？
**Answer** 新建(NEW)：新创建了一个线程对象。
           可运行(RUNNABLE)：线程对象创建后，其他线程(比如main线程）调用了该对象的start()方法。
                         该状态的线程位于可运行线程池中，等待被线程调度选中，获取cpu 的使用权 。
           运行(RUNNING)：可运行状态(runnable)的线程获得了cpu 时间片（timeslice），执行程序代码。
           阻塞(BLOCKED)：阻塞状态是指线程因为某种原因放弃了cpu 使用权，也即让出了cpu timeslice，暂时停止运行。
                          直到线程进入可运行状态，才有机会再次获得cpu timeslice 转到运行状态。
           死亡(DEAD)：线程run()、main() 方法执行结束，或者因异常退出了run()方法，则该线程结束生命周期。死亡的线程不可再次复生。

5. 掷一枚不均匀的硬币，正面概率为0.7，反面的概率为0.3，如何最高效地获得一个概率为0.5的事件？
**Answer** 每次掷两次硬币，如果结果是 01 或者 10 就 accept，结果是 00 或者 11 就 reject。
           如果得到01就甲喝水，如果得到10就乙喝水。
           
           
- 编程
有一个整数数组：15，3，10，9，6，5，4，8，13，16
求：第一个间断的数，例如上述数组是7
要求：时间复杂度O(N)，空间复杂度：尽可能小
**Answer**
![Image text](https://github.com/saengsawang/img-storage/blob/master/字节二面间断数解答.png)

```
