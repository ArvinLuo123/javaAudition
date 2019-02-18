
# java面试知识点

<br>

### 网络知识
* [TCP的三次握手](#TCP的三次握手)
* [TCP的四次挥手(断开时)](#TCP的四次挥手(断开时))
* [TCP的滑动窗口](#TCP的滑动窗口)
* [超文本传输协议HTTP](#超文本传输协议HTTP)
* [在浏览器键入url,按下回车之后经历的流程](#在浏览器键入url,按下回车之后经历的流程)
* [HTTP状态码](#HTTP状态码)
* [GET请求和POST请求的区别](#GET请求和POST请求的区别)
* [Cookie和Session的区别](#Cookie和Session的区别)
* [HTTP和HTTPS的区别](#HTTP和HTTPS的区别)

### 关系型数据库
* [如何设计一个关系型数据库](#如何设计一个关系型数据库)
* [索引模块](#索引模块)
* [索引的数据结构](#索引的数据结构)
* [密集索引和稀疏索引的区别](#密集索引和稀疏索引的区别)
* [如何定位并优化慢查询sql](#如何定位并优化慢查询sql)
* [联合索引的最左匹配原则的成因](#联合索引的最左匹配原则的成因)
* [索引是建立的越多越好么](#索引是建立的越多越好么)
* [锁模块](#锁模块)
* [MyISAM与InnoDB关于锁方面的区别是什么](#MyISAM与InnoDB关于锁方面的区别是什么)
* [数据库锁的分类](#数据库锁的分类)
* [数据库事务的四大特性ACID](#数据库事务的四大特性ACID)
* [事务隔离级别以及各级别下的并发访问问题](#事务隔离级别以及各级别下的并发访问问题)
* [InnoDB可重复读隔离级别在如何避免幻读](#InnoDB可重复读隔离级别在如何避免幻读)

### 缓存知识考点
* [缓存中间件Memcache和redis的区别](#缓存中间件Memcache和redis的区别)
* [为什么Redis这么快](#为什么Redis这么快)
* [说说你用过的Redis的数据类型](#说说你用过的Redis的数据类型)
* [从海量key里查出某一固定前缀的key](#从海量key里查出某一固定前缀的key)
* [如何使用Redis做异步队列](#如何使用Redis做异步队列)
* [Redis如何做持久化](#Redis如何做持久化)
* [使用Pipeline的好处](#使用Pipeline的好处)
* [Redis的读写分离同步机制](#Redis的读写分离同步机制)
* [如何将不同的key均匀放在不同的redis集群节点](#如何将不同的key均匀放在不同的redis集群节点)

### Linux
* [Linux的体系结构](#Linux的体系结构)
* [查找特定的文件](#查找特定的文件)
* [根据文件内容去筛选](#根据文件内容去筛选)
* [对文件内容做统计](#对文件内容做统计)

### JVM
* [JVM如何加载class文件](#JVM如何加载class文件)
* [什么是反射](#什么是反射)
* [谈谈ClassLoader](#谈谈ClassLoader)
* [类的加载方式](#类的加载方式)
* [Java的内存模型](#Java的内存模型)
* [JVM三大性能调优参数](#JVM三大性能调优参数)
* [Java内存模型中堆和栈的区别](#Java内存模型中堆和栈的区别)
* [元空间/堆/线程独占部分的联系](#元空间/堆/线程独占部分的联系)
* [不同JDK版本间intern方法的表现](#不同JDK版本间intern方法的表现)

### GC

* [Java对象被判定为垃圾的标准是什么](#Java对象被判定为垃圾的标准是什么)
* [判定对象是否为垃圾的算法](#判定对象是否为垃圾的算法)
* [垃圾回收的算法](#垃圾回收的算法)
* [分代收集算法(Generational-Collector)](#分代收集算法(Generational-Collector))
* [GC中什么是Stop-the-World](#GC中什么是Stop-the-World)
* [什么是Safepoint](#什么是Safepoint)
* [JVM的运行模式](#JVM的运行模式)
* [常见的垃圾收集器](#常见的垃圾收集器)
* [Object的finalize()方法的作用是否与C++的析构函数作用相同](#Object的finalize()方法的作用是否与C++的析构函数作用相同)
* [Java中的强引用,软引用,弱引用,虚引用](#Java中的强引用,软引用,弱引用,虚引用)
* [引用队列(ReferenceQueue)的作用](#引用队列(ReferenceQueue)的作用)


### 消息队列
* [为什么要引入消息中间件](#为什么要引入消息中间件)
* [引入消息中间件之后会有哪些缺点](#引入消息中间件之后会有哪些缺点)
* [如果消费者接收到消息,完成消息之前宕机怎么办?](#如果消费者接收到消息,完成消息之前宕机怎么办?)
* [在某次高峰期间MQ中间件故障的情况下的卡死情况](#在某次高峰期间MQ中间件故障的情况下的卡死情况)
* [如何保证消息中间件里的消息不会丢失? (消息的持久化)](#如何保证消息中间件里的消息不会丢失? (消息的持久化))
* [如何保证消息中间件全链路数据100%不丢失](#如何保证消息中间件全链路数据100%不丢失)
* [分析一下消费者手动ack机制保证消息不丢失的底层原理](#分析一下消费者手动ack机制保证消息不丢失的底层原理)
* [消息中间件的生产端如何保证数据不丢失](#消息中间件的生产端如何保证数据不丢失)
* [消息中间件全链路100%数据不丢失(三个方面)](#消息中间件全链路100%数据不丢失(三个方面))


### Java常用类库
* [Error和Exception的区别](#Error和Exception的区别)
* [Java的异常体系](#Java的异常体系)
* [常见的Error以及Exception](#常见的Error以及Exception)
* [数据结构和算法考点](#数据结构和算法考点)
* [Java集合](#Java集合)
* [HashMap/HashTable/ConcurentHashMap的区别](#HashMap/HashTable/ConcurentHashMap的区别)
* [Java8前后HashMap的区别](#Java8前后HashMap的区别)
* [HashMap的put方法](#HashMap的put方法)
* [HashMap如何减少碰撞以提高效率](#HashMap如何减少碰撞以提高效率)
* [HashMap扩容的问题](#HashMap扩容的问题)
* [什么是HashTable](#什么是HashTable)
* [什么是ConcurrentHashMap](#什么是ConcurrentHashMap)
* [CountDownLatch和CyclicBarrier的区别](#CountDownLatch和CyclicBarrier的区别)
* [BIO/NIO/AIO的区别](#BIO/NIO/AIO的区别)



<br>

<h2 id="网络知识">网络知识</h2>

<br>

   <h3 id="TCP的三次握手">TCP的三次握手</h3>  
   
   TCP是属于传输层的协议,抓包的工具Wireshark  
    
   * 三次握手的流程如下:  
   1) 第一次握手,建立连接时,客户端发送SYN包(syn=j)到服务器,并进入SYN_SEND状态,等待服务器确认;  
   2) 第二次握手,服务器收到SYN包,必须确认客户的SYN,同时自己也发送一个SYN包(syn=k),即SYN+ACK(ack=j+1)包,此时服务器进入SYN_RECV状态.  
   3) 第三次握手,客户端收到服务器的SYN+ACK包,向服务器发送确认包ACK(ack=k+1),此包发送完毕,客户端和服务器进入ESTABLISHED状态,完成三次握手.
         
   * 为什么需要三次握手才能建立起连接?   
     为了初始化Sequence Number的初始值(即上面的j和k),以保证信息传输过程中不会乱序.所以在服务器发送了Sequence Number后(第二次握手),需要客户端发送确认报文给服务器,告知已收到其初始化的Sequence Number了.
         
   * 首次握手的隐患--SYN超时问题  
     Server收到Client的SYN,回复SYN-ACK的时候未收到ACK确认.Server会不断重试直至超时,Linux默认重试5次,每次等待时间翻倍(2+4+8+16+32),总共等待63秒才断开连接.会是server招到SYN Flood攻击,将服务器的连接数耗尽,不能处理正常的连接请求.
           
   * Liunx下针对SYN Flood的防护措施:   
     SYN队列满后,Server会通过TCP的一个特殊的tcp_syncookies参数(请求地址+目标地址+时间戳组成)会发SYB Cookie,若为正常连接Client是会有响应的,会回发SYN Cookie,在即使SYN队列满的情况下,也能建立连接.  
          
   <h3 id="TCP的四次挥手(断开时)">TCP的四次挥手(断开时)</h3>  
   
   * 第一次挥手:Client发送一个FIN,用来关闭Client到Server的数据传送,Client进入FIN_WAIT_1状态;  
   * 第二次挥手:Server收到FIN后,发送一个ACK给Client,确认序号为收到序号+1(与SYN相同,一个FIN占用一个序号,Server进入CLOSE_WAIT状态);  
   * 第三次挥手:Server发送一个FIN,用来关闭Server到Client的数据传送,Server进入LAST_ACK状态;  
   * 第四次挥手:Client收到FIN后,Client进入TIME_WAIT状态,接着发送一个ACK给Server,确认序号为收到序号+1,Server进入一个CLOSED状态,完成四次挥手.  
   * 为什么需要四次挥手才能断开连接?  
     因为全双工,发送方和接收方都需要FIN报文和ACK报文.  
   * 服务器中出现大量CLOSE_WAIT状态的原因?  
     Client关闭socket连接,Server没有及时关闭连接,可能情况:1)缺少一些释放资源的代码; 2)处理请求的线程配置不合理.  
     
   <h3 id="TCP的滑动窗口">TCP的滑动窗口</h3>  
   
   * RTT: 发送一个数据包到收到对应的ACK,锁花费的时间.   
   * RTO: 重传的时间间隔,是根据RTT的值动态计算的.   
   * TCP传输过程中是把数据分为一段一段传输的,我们不能上一段被确认之后再发送下一段.要批量的发送,就要解决可靠传输和包乱序的问题. TCP使用滑动窗口做流量控制与乱序重排.
     
   <h3 id="超文本传输协议HTTP">超文本传输协议HTTP</h3>  
    
   1.1相比1.0 : 引入keep-alive机制.以前是close
   若为close,是服务器主动关闭连接,若为keep-alive,则连接会保持一段时间不会立刻关闭,在此期间还可以数据传输.      
     
   <h3 id="在浏览器键入url,按下回车之后经历的流程">在浏览器键入url,按下回车之后经历的流程</h3> 
   
   1) 会依据url逐层查询DNS缓存,解析url中的域名对应的ip地址. 浏览器缓存-->系统缓存-->路由器缓存-->服务器缓存  
   2) 根据ip地址和端口(默认80)与服务器建立TCP连接  
   3) 浏览器发送http请求  
   4) 服务器对http请求做出响应  
   5) 浏览器解析渲染html  
   6) 浏览器释放TCP连接,四次挥手   
     	
   <h3 id="HTTP状态码">HTTP状态码</h3> 
   
   1xx: 指示信息--表示请求已接收,继续处理  
   2xx: 成功--表示请求已被成功接收  
   3xx: 重定向--要完成请求必须进行进一步转发  
   4xx: 客户端错误--请求有语法错误或请求无法实现  
   5xx: 服务端错误--服务端未能实现合法的请求  
   400 Bad Request: 客户端有语法错误,不能被服务器所理解  
   401 Unauthorized: 请求未经授权,这个状态码必须和www-Authenticate报头域一起使用.  
   403 Forbidden: 服务器接收到请求,但是由于某些原因(ip被禁)拒绝提供服务.  
   404 NOT FOUND: 请求资源不存在,输入了错误的url.  
   500 Internal Server Error: 服务器内部发生不可逾期的错误(代码写的有问题)  
   503 Server Unavaiable : 服务器当前不能处理客户端请求(比如连接池占用满了),一段时间后可能恢复正常    
   	
   <h3 id="GET请求和POST请求的区别">GET请求和POST请求的区别</h3> 
   
   1. HTTP报文层面:  
     GET将请求信息放在url中,POST放在请求体中,所以POST请求没有长度限制,GET请求会有一些长度限制.  
   2. 数据库层面:  
     GET都是查询请求,符合数据的幂等性和安全性,POST会修改数据库,不符合  
   3. 缓存层面:  
     GET请求可以被缓存,被存储,而POST不行.所以绝大部分GET请求会被CDN缓存,大大减少web服务器压力,而POST是非幂等的,必须交由web服务器来处理  
    CDN缓存:  
     客户端浏览器先检查是否有本地缓存是否过期，如果过期，则向CDN边缘节点发起请求，CDN边缘节点会检测用户请求数据的缓存是否过期，如果没有过期，则直接响应用户请求，此时一个完成http请求结束；如果数据已经过期，那么CDN还需要向源站发出回源请求（back to the source request）,来拉取最新的数据。  
     
   <h3 id="Cookie和Session的区别">Cookie和Session的区别</h3> 
   
   * Cookie: 由服务器发给客户端的特殊信息,以文本的形式存放在客户端存放在response header中,客户端再请求浏览器就会携带上这些信息.  
   * Session: 在服务器上保存的信息.解析客户请求并生成操作session,sessionId.  
   * session的实现方式:  
     1) 通过Cookie来传输JSESSIONID-xxx  
     2) 使用url回写来实现,服务器发送给浏览器的所有链接中都包含JSESSIONID,客户端点击任何一个链接都可以吧JSESSIONID带回浏览器.单独输入链接地址请求是不会携带JSESSIONID.  
     tomcat两种实现方式都支持,如果浏览器禁用Cookie,则使用url回写.  
   * 区别:  
    Cookie数据存放在浏览器上,Session数据存放在服务器上.所以Cookie数据不安全,容易被认为使用造假进行Cookie欺骗,Session相对安全 . 考虑到减轻服务器负担推荐使用Cookie.
       
   <h3 id="HTTP和HTTPS的区别">HTTP和HTTPS的区别</h3>  
    
   * HTTPS:  
     在HTTP下加了一层SSL(Sercurity Sockets Layer,安全套接层,SSL3.0后更名为TLS),对传输信息进行加密.      
   
   * HTTPS数据传输流程:  
    1) 浏览器将支持的加密算法信息发送给服务器  
    2) 服务器选择一套浏览器支持的加密算法,以证书的形式回发浏览器  
    3) 浏览器验证证书的合法性,并结合证书公钥加密信息发送给服务器  
    4) 服务器使用私钥解密信息,验证哈希,加密响应消息回发浏览器.  
    5) 浏览器解密响应消息,并对消息进行验真,之后进行加密数据的交互.    
    
   * HTTP和HTTPS的区别:  
    1. HTTPS需要到CA申请证书,HTTP不需要.  
    2. HTTPS密文传输,HTTP是明文传输  
    3. HTTPS默认使用443端口,HTTP使用80端口  
    4. HTTPS=HTTP+加密+认证+完整性保护,较HTTP安全  
   SOCKET简介:  
     Socket是对TCP/IP的抽象,是操作系统对外开放的接口.


<br>

<h2 id="关系型数据库">关系型数据库</h2>

<br>
   
   <h3 id="如何设计一个关系型数据库">如何设计一个关系型数据库</h3>   
   
   ![设计一个数据库](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/%E8%AE%BE%E8%AE%A1%E4%B8%80%E4%B8%AA%E6%95%B0%E6%8D%AE%E5%BA%93.png "设计一个数据库")
     
   分为两部分:  
   		存储部分:将数据通过I/O持久化到磁盘上.I/O持久化是数据库速度的瓶颈,所以我们需要程序实例部分对存储部分进行管理和优化.  
   		程序实例:  
   * 存储管理:将物理关系映射为逻辑关系.  
   * 缓存机制:优化执行效率,会缓存之前查询到的结果以及其相关结果  
   * SQL解析:将SQL语句进行解析  
   * 日志管理:记录操作,以便主从同步及数据恢复  
   * 权限划分:进行多用户管理的权限划分模块  
   * 容灾机制:灾难恢复模块  
   * 索引管理:优化数据查询效率  
   * 锁管理:使数据库支持并发操作  
   	数据库的开发其实与我们平时的开发的项目一样,模块也相似,是经典的架构.  
   	
   <h3 id="索引模块">索引模块</h3>
   
   * 为什么要使用索引?  
   		避免全表扫描,提升查找效率,思想来源于字典,通过关键信息来快速定位.  
   
   * 什么样的信息可成为索引?  
   		把该记录限定在一定查找范围内的字段(关键字).比如主键/唯一键/普通键
   
   <h3 id="索引的数据结构">索引的数据结构</h3>
   
   * 二叉树查找树  
       平衡二叉树:任意结点的左子树和右子树的高度差不超过1.  
       当数据删除,新增比较多的时候,现有的结构会发生打乱,二叉查找树会被打乱成为线性的.假定二叉树全都存在磁盘中,查找深度每增加1就要多进行一次IO操作,这样数据一多,数的深度就会很深,会增加IO次数,速度反而不如全表扫描来的快(全表扫描是每次读一页或者一块的数据进来),所以要让树变得矮一些,每阶层结点存储的数据多一些.要用到B-Tree了  
   
   * B-Tree(平衡多路查找树)见图.   
   ![B-Tree结构图](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/B-Tree%E7%BB%93%E6%9E%84%E5%9B%BE.png "B-Tree结构图")  
   
        每个节点包括:关键字(索引字段)+每个子节点的指针.  
        每个结点有几个孩子就是几阶B树,比如三阶B树.除根节点和叶子节点(没有子节点的节点)以外,其他每个节点至少有ceil(m/2)个孩子.所有叶子节点都位于同一层.  
        当数据删除,新增比较多的时候,B树通过它的规定来保持树的特征.使得查询复杂度保持在O(logn).  
   
   * B+-Tree(Mysql中用)见图    
   ![B+-Tree结构图](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/B%2B-Tree%E7%BB%93%E6%9E%84%E5%9B%BE.png "B+-Tree结构图")
   
        B+是B的变体,基本定义与B树相同,除了:  
        非叶子节点的子树指针与关键字个数相同:可以存更多关键字,树更矮  
        非叶子节点的子树指针P[i],指向关键字[K[i],K[i+1])的子树.  
        非叶子节点仅用来索引,数据都保存在叶子节点中:非叶子节点只能用来存索引,指针,意味着B+-Tree可以存更多的索引,可以变得更矮.所有的搜索都在叶子节点中终结.  
        所有叶子节点均有一个链指针指向下一个叶子节点,并且按大小顺序排布:查询到范围的端点以后便通过链接找到之前或之后所有数据,便于范围的统计  
   
   * B+Tree更适合来做存储索引:   
      磁盘读写代价更低.(一次加载更多的关键字,减少IO读写次数)  
      查询效率更加稳定.(所有的搜索都会走一遍根节点到叶子节点的过程,查询不同元素复杂度都为O(logn))  
      更有利于数据库的扫描,数据都保存在叶子节点中,并且有链指针链接,便于范围查找统计.  
   
   
   * Hash索引: 见图  
   ![hash索引](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/hash%E7%B4%A2%E5%BC%95.png "hash索引")
   
   所查数据根据hash计算只需一次便可定位到查找数据所在的bucket,之后将bucket中的entry(链表)全部加载进入内存,顺着链表指针找到所需的数据.理论上比B+Tree查询效率高.   

   缺点:  
   1. 仅仅能满足=,in,不能用范围查询: hash索引比较的是hash运算之后的hash值,只能用于等值过滤,因为经过计算hash值与原来的大小关系不一定相同,不同的值可能计算出相同的hash值,所以不能用于范围查询.  
   2. 数据库无法用索引来避免排序操作:因为索引是计算后的hash值,大小关系不一定相同.  
   3. 做组合索引时,hash索引不能利用部分索引来查询.B+Tree支持.  
   4. 不能避免表扫描,因为根据索引找到bucket之后必须要扫描bucket中的数据来查找.  
   5. 遇到大量hash值相等的情况后性能不一定比B+Tree高,因为大量的数据指针会存到同一个bucket中.  
   
   * BitMap位图索引: (Oracle支持)   
       表中的某个字段只有几种枚举值时,十分适用.不适合高并发多的系统,适合统计多的系统.
       
   <h3 id="密集索引和稀疏索引的区别">密集索引和稀疏索引的区别</h3>  
     
   ![密集索引和稀疏索引](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/%E5%AF%86%E9%9B%86%E7%B4%A2%E5%BC%95%E5%92%8C%E7%A8%80%E7%96%8F%E7%B4%A2%E5%BC%95.png "密集索引和稀疏索引")
    
   密集索引: 每个搜索码都对应一个索引值.叶子结点中不仅保存键值还保存了该列的数据.一个表只能创建一个密集索引.  
   稀疏索引:
       只为索引码的某些值建立索引项.叶子结点只保存了键值以及该行数据的地址或者主键信息.找到叶子结点以后仍要通过地址或者主键信息来寻找数据.
   
   * 对Mysql分析:  见图  
   ![InnoDB与MyISAM](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/InnoDB%E4%B8%8EMyISAM.png "InnoDB与MyISAM")
   
       MyISAM: 表的所有类型的索引都用稀疏索引,索引与数据是分两个文件存储的.  
       InnoDB: 表有且仅有一个密集索引,其他索引都是稀疏索引(辅助键索引),索引与数据是在一个文件存储的.  
       
       密集索引规则:
        1) 有主键,该主键则作为密集索引  
        2) 没有主键,表的第一个唯一非空索引作为密集索引  
        3) 都没有,InnoDB会生成一个隐藏主键作为密集索引  
        4) 其他的稀疏索引(辅助键索引),其叶子结点会存储键值以及主键值,然后在通过主键值去密集索引里查找.  

       在mysql的根目录data文件下数据库里可以找到表相关文件:  
           xxx.frm存储的是表结构信息.  
           xxx.ibd是InnoDB下索引与数据的存储文件.  
           xxx.MYI是MyISAM下存储索引的文件.  
           xxx.MYD是MyISAM下存储数据的文件.  
    
   
   * 衍生出来的问题,以mysql为例:  

   <h3 id="如何定位并优化慢查询sql">如何定位并优化慢查询sql</h3>    
   
   1. 根据慢日志定位查询慢sql  
        在my.ini(windows环境下)配置文件里修改慢日志的一些参数.  
        一条sql查询时间超过1s就是慢的.  
        一旦mysql重启,慢sql日志就会被清零.  
        
   2. 用explain来分析慢sql   
       在查询语句的前面加上explain即可.  
       Explain关键字段:  
       id字段:  指查询顺序,在复合查询里面,id越大的越先执行.  
       type字段:    
        system > const > eq_ref > ref > fulltext > ref_or_null > index_merge > unique_subquery > index_subquery > range > index > all  
        当type是index/all时,意味着sql进行了全表扫描,需要优化.  
       extra字段:  
        extra中出现以下2项意味着MYSQL根本不能使用索引,效率会受到重大影响,需要优化:  
        Using filesort--表示MYSQL会对结果使用一个外部索引排序,而不是使用本表的索引,可能在内存或者磁盘上进行排序.MYSQL中无法利用索引完成的排序操作称为"文件排序".  
        Using temporary--表示MYSQL在对查询结果排序时使用临时表,常见于排序order by 和 分组查询group by  
        
   3. 修改sql或者尽量让sql走索引  
        EXPLAIN SELECT COUNT(id) FROM `repayment` ORDER BY create_time DESC; 查询时没有走主键索引,而是根据查询优化来选择走哪个索引.   
        EXPLAIN SELECT COUNT(id) FROM `repayment` ORDER BY create_time DESC force index(primary)强制用主键索引. 

   <h3 id="联合索引的最左匹配原则的成因">联合索引的最左匹配原则的成因</h3>   

   最左匹配原则:   
   1. mysql会一直向右匹配知道遇到范围查询(>,<,between,like)就停止匹配,比如a=3 and b=2 and c >5 and d =6 如果建立(a,b,c,d)顺序的联合索引,d是用不到索引的,如果建立(a,b,d,c)的联合索引就可以用到,a,b,d的顺序可以任意调整.  
   2. =和in可以乱序,比如a=1 and b=2 and c=3 建立(a,b,c)索引可以任意顺序,mysql的查询优化器会帮你优化成索引可以识别的形式.  

   原因:  
    创建联合索引时,先对最左边的字段进行排序,在第一个排序的基础上再对第二个索引字段进行排序.直接用第二个字段是用不到索引的.  
    建立联合索引的时候,把可能范围查询的字段放在后面.

   <h3 id="索引是建立的越多越好么">索引是建立的越多越好么</h3>    
   1. 数据量小的表不需要建立索引,建立会增加额外的索引开销.  
   2. 数据变更需要维护索引,更多的索引意味着更多的维护成本.  
   3. 更多的索引意味着需要更多的空间.  
   
   <h3 id="锁模块">锁模块</h3>
   
   
   <h3 id="MyISAM与InnoDB关于锁方面的区别是什么">MyISAM与InnoDB关于锁方面的区别是什么</h3>
   
   MyISAM只支持表级锁,而InnoDB支持行级锁,也支持表级锁.  

   lock tables person_info read/write;   //给表加读锁或写锁  
   unlock tables;  //释放锁  

   读锁:是共享锁,上读锁以后仍然可以读操作,但不可以写操作.即上共享锁之后可以伤共享锁,不能上排它锁.  
   写锁:是排它锁,上了写锁以后既不能读操作也不能写操作.即上了排它锁之后不能上共享锁也不能上排它锁.  

   给读操作上排它锁:  
   select * from person_info where id = 111 for update.

   InnoDB用的是二段锁,即运行时加锁,然后commit提交来解锁,默认是自动提交事务的,通过下面的命令去除自动提交事务:   
   commit;  提交事务  
   
   show variables like 'autocommit'; 为on表示自动提交已经开启.  
   set autocommit = 0; 关闭自动提交.  

   InnoDB对select有改进,查询时不加读锁.要想select加入读锁,执行:  
    select * from person_info where id = 3 lock in share mode; 无法加入排它锁  
    commit;  之后可以加入排它锁  

   InnoDB当sql不走索引的时候,整张表就会被锁住,也就是用的表级锁.当sql走索引的时候,用的行级锁或者gap锁.  
   
   MyISAM适合的场景:  
   1. 频繁执行全表count语句,因为MyISAM有一个变量来存储表数据的行数,而InnoDB没有.
   2. 对数据进行增删改的频率不高,查询非常频繁
   3. 不用事务的场所. 
    
   InnoDB适合的场景:  
   1. 数据增删改查都相当频繁.
   2. 可靠性有求比较高,要求支持事务.  

   <h3 id="数据库锁的分类">数据库锁的分类</h3>

   * 按锁的粒度划分:表级锁,行级锁,页级锁
       
   * 按锁级别划分:共享锁,排它锁    
     
   * 按加锁方式划分:自动锁,显示锁  
       自动锁: insert,update,detele以及MyISAM的表锁,这是Mysql自动为我们上的.  
       显示锁: select for update , lock in share mode这些我们显示加的锁.  
       
   * 按操作划分: DML锁(多数据操作),DDL锁(对表结构操作) .    
       
   * 按使用方式划分: 乐观锁,悲观锁  
        悲观锁:   
        对外界的修改持保守态度,依靠数据库提供的锁机制,在数据处理全程中用排它锁锁定(悲观锁的一种实现方式),即先取锁再访问的保守策略,数据的安全有保障,但是会增加数据库的开销,增加产生死锁的几率.      
  		乐观锁:   
  		认为外界的修改不会造成冲突,在数据提交时才会对数据的冲突与否进行检测,若发现错误则返回错误的信息,让用户决定怎么做.乐观锁并不使用数据库提供的所机制,采用记录数据版本(1.用版本号记录version(int) 2.用时间戳记录)的方式来实现.      	
  		先读取数据,得到version的值为versionValue;   
  		每次更新数据的时候,为了防止冲突,先去检查version再做更新,更新成功的话version+1,冲突的话将失败信息返回给用户.    
  		认为数据之间冲突的可能性较小,在提交时才检查版本,而不是在提交之前就锁住数据.不会产生死锁.  
  		类似CAS机制??  

   <h3 id="数据库事务的四大特性ACID">数据库事务的四大特性ACID</h3>   
   
  * 原子性(Atomic):  
  	  事务包含的所有操作要么全部执行,要么全部不执行.  
  * 一致性(Consistency):  
  	  事务应确保数据库状态从一个一致的状态转变为另外一个一致的状态, 比如A和B无论怎么转账,两者的金额之和不变.   
  * 隔离性(Isolation):  
      多个事务并行执行时,一个事务的执行不能影响其他事务的执行.  
  *	持久性(Durability):  
  	  一个事务一旦提交它对数据库的修改应该永久性的保存在数据库中,即当数据库发生故障时,确保已经提交的事务不能丢失.  


   <h3 id="事务隔离级别以及各级别下的并发访问问题">事务隔离级别以及各级别下的并发访问问题</h3>   
   
   1. 更新丢失--mysql的InnoDB引擎有很多的事务隔离级别,使得在数据库层面可可以避免   
   2. 脏读:一个事务读到另一个事务未提交的更新数据. --READ-COMMITTED已提交读事务隔离级别上可以避免,Oracle默认的事务隔离级别READ-COMMITTED   
       select @@tx_isolation;     // 	查看事务的隔离级别  
       set session transaction isolation level read uncommitted;   // 设置当前session级别为读未提交  
   3. 不可重复读: 事务a多次读取同一数据,事务b在事务a多次读取的过程中做了更新提交,使a多次读取时结果不一致.  
    --REPEATABLE-READ可重复读事务隔离级别以上可以避免,Mysql的InnoDB默认事务隔离级别REPEATABLE-READ  
   4. 幻读: 事务a读取与搜索条件相匹配的若干行,事务b以插入或者删除行来修改事务a的结果集,导致事务a再执行当前读操作,出现幻行(比如原来读共有3行,然后全局update,竟然更新了4行).  
    --SERIALIZABLE串行事务隔离级别可以避免.  
    
   <h3 id="InnoDB可重复读隔离级别在如何避免幻读">InnoDB可重复读隔离级别在如何避免幻读</h3>   
   
   * 表象:快照读(非阻塞读)---伪MVCC,多版本并发控制(因为没有实现多版本共存)   
   
        当前读: 读取的是最新记录,并且保证读到的数据不能被其他数据修改,加锁.   
        加了锁的增删改查   
        select...lock in share mode , select...for update , update , delete , insert   

        快照读: 不加锁的非阻塞读(事务隔离级别不为SERIALIZABLE,SERIALIZABLE为串行读,快照退化为当前读)  
        select  

        在RC隔离级别下,当前读和快照读读到的数据是一样的,在RR隔离级别下,如果先快照读,再更新,快照读可能读到修改之前的数据. 如果更新完再快照读,就会读到最新版本,也就是在RR级别下快照读的时机很重要  
        RC,RR级别下的InnoDB的快照读如何实现?  
        --数据行里的DB_TRX_ID(事务) , DB_ROLL_PTR(回滚) , DB_ROW_ID的字段  
        --undo日志(老版本的记录回滚时候用,分为insert的undo,update的undo)  
        --read view 判断快照读能看哪个版本的数据  
        将要修改的数据的SB_TRX_ID取出来,与系统其它活跃事务id做对比,如果>=这些id的话,就根据DB_ROLL_PTR指针去取出undo日志中上一层的DB_TRX_ID,知道小于这些活跃事务id,保证我们获取到的数据版本是当前可用的最稳定版本.  
        再一次事务内,RR首次快照读会创建一个read view , 此后在调用快照读时,用的还是同一个read view , 在RC中每次快照读都会重新创建一个快照 . 所以RR select --> update -->select 可能读到旧数据.  

   * 内在:next-key锁(行锁+gap锁)   
   
       Gap锁: 锁一定范围间隙内的数据,比如delete,id=9的数据(未命中),此时你插入id=10,就会因为gap锁而失效.  
       RR以及Seriaizable隔离级别下,默认都支持gap锁.  

       Gap锁的触发?  
        如果where条件全部命中,则不会用Gap锁,只会加记录所锁,就能保障不幻读.  
        如果where条件部分命中或者全不命中,则会增加Gap锁.  
       Gap锁会用在非唯一索引或者不走索引的当前读.比如delete,id=9(id非唯一索引),此时会触发Gap锁,锁住(6,9],(9,11]的区间(临界点也与主键的值有关),此时另一个session想要插入id=9的数据会失败,直到该事务提交或者回滚.防止了幻读.不然会出现delete前只有一条,delete完之后有两条数据被删除的情况.不走索引的情况,会触发所有的Gap锁,这样比全表锁的效率更低,因此要避免这种情况.
       
   <h3 id="复杂的sql语句写法">复杂的sql语句写法</h3>          
   * group by / having   
  	   统计相关: COUNT , SUM , MAX , MIN , AVG   

   * group by  
     1. 满足 "select子句中的列名必须为group by里用到的列或者sum,min等列函数的列"只针对同一张表成立,联查时不成立.  
  	 2. 列函数对于group by 子句定义的每个组各返回一个结果.  
  	   group by会把结果集缓存在一张临时表里,然后再通过统计函数对这些结果集进行统计,再展现出来.  

   * having   
     1. 通常与group by子句一起使用 , 没有groupby,having与where作用相同.   
   	 2. where过滤行,having过滤组  
  	 3. 出现在同一sql的顺序: where > group by > having  

   * 查询平均成绩大雨60分的同学的学号和平均成绩: 
     
<pre>
  	select
  		student_id , avg(score)
	from score
	group by student_id
	having avg(score) > 60 ;
	
</pre>  

   * 查询没有学全所有课的同学的学号,姓名:   
   
<pre> 
  	select
  		stu.student_id,
  		stu.name
  	from student stu, score s
  	where stu.student_id = s.student_id
  	group by student_id
  	having count(*) >
  	( select count(*) from course ) ;
</pre>  
  学习一下数据库的理论范式.



<br>

<h2 id="缓存知识考点">缓存知识考点</h2>

<br>

   缓存穿透 : 要查的数据缓存里没有,去数据库里查,然后回写存储在缓存层.

   <h3 id="缓存中间件Memcache和redis的区别">缓存中间件Memcache和redis的区别</h3>  
    
   Memcache :
   1. 支持简单数据类型
   2. 不支持数据持久化
   3. 不支持主从
   4. 不支持分片   
   
   Redis :
   1. 数据类型丰富
   2. 支持数据磁盘持久化存储
   3. 支持主从
   4. 支持分片


   <h3 id="为什么Redis这么快">为什么Redis这么快</h3>  
   
   支持10w+ QPS (query per second , 每秒内查询次数)
   1. 完全基于内存,绝大部分请求时纯粹的内存操作,执行效率高.
   2. 数据结构简单,非关系型数据库,存储结构就是键值对,类似于hashMap,查找的时间复杂度为O(1).
   3. 采用单线程,单线程也能处理高并发请求,避免了锁竞争,没有线程安全问题,想多核可以启动多个redis实例.
   4. 使用多路I/O复用模型,非阻塞I/O:   
        FD: File Descriptor , 文件描述符: 一个打开的文件通过唯一的描述符进行引用,该描述符是打开文件的元数据到文件本身的映射.   
        * 传统的阻塞I/O模型:   
        当对某个文件FD进行读写时,如果该FD不可读/写,整个服务就不会对其他操作响应.   
        * 多用I/O复用模型:   
        Select系统调用:select模型可以同时监控多个文件FD的可读/可写情况,然后程序就可以做别的事情而不被阻塞了.   
        redis会依据操作系统的不同选用不同的多路复用函数(epoll,kqueue,evport,select),优先选择时间复杂度为O(1)的I/O多路复用函数,如果没有就选择时间复制读为O(n)的select作为保底.  


   <h3 id="说说你用过的Redis的数据类型">说说你用过的Redis的数据类型</h3>  
   
   1. String : 最常用的key-value形式 , value最大存512M的数据,二进制安全(可以存JPEG图像,序列化的对象)   
            redis中每一个操作都是原子性的,所以可以不用考虑并发性,用incr来计数.例如:想统计用户每天访问网站的次数,可以用userId+日期作为key,每次用户访问,redis就执行一次incr来计数.   
   2. Hash : String类型的field-value的映射,适合用于存储对象.   
            创建一个lilei的映射 : hmset lilei name "LiLei" age 26 title "Senior"   
            查name字段 :  hget lilei age   
            修改title字段 : hset lilei title "Pricipal"    
   3. List : 按照String元素插入顺序排序 , 后进先出(类似于stack,实现最新消息排行榜等功能) , 可存40亿数据    
            给mylist中插入数据 : lpush mylist aaa   
            查看mylist中数据 : lrange mylist 0 10  (从左往右取出第0位到第10位)   
   4. Set : String元素组成的无序集合 , 通过hash实现(所以查找,新增,删除一个元素的时间复杂度是O(1)),不允许重复.   
            添加元素 : sadd myset 111   
            查看myset中的元素 : smembers myset   
          redis可以求出两个集合的交集并集差集等功能,实现共同关注,共同喜好等功能.   
   5. Sorted Set : String元素的有序不重复集合,每个元素对应一个分数,通过分数来为集合中成员从小到大排序.   
            给zset中添加元素 : zadd myset 3 abc  (添加时指定元素对应的分数)  
            查看zset中数据 : zrangebyscore myzset 0 10  (从左往右取出第0位到第10位)   
           用Sorted Set来做带权重的队列,比如普通消息的score为1 , 重要消息的score为2 , 工作线程也可按工作的大小获取消息,让重要的任务优先执行.   
   6. 除了以上5个常用的以外,还有用于计数的HyperLogLog , 用于支持存储地理位置信息的Geo.  
   
  
   <h3 id="从海量key里查出某一固定前缀的key">从海量key里查出某一固定前缀的key</h3>   
      
   1. 要先问清数据规模,问清边界.  
   2. keys pattern : 查找出符合给定模式pattern的key.  
            keys k1*   
            keys指令一次性返回所有匹配的key,key的数量过大会使服务卡顿.   
   3. 若redis正在给线上提供服务,使用keys指令会有什么问题?   
           会使redis服务卡顿   
   4. 用SCAN指令,无阻塞地提取key列表:   
            SCAN cursor(游标) [MATCH pattern] [COUNT count]       
            
         1. 基于游标的迭代器,需要基于上一次的游标延续之前的迭代过程.返回值:当前遍历到的游标,以及查询到的数据.  
         2. 以0作为游标开始新的迭代,直到命令返回游标0完成一次遍历.  
         3. 不保证每次执行都返回某个给定数量的元素,支持模糊查询.  
         4. 一次返回的数量不可控,只能是大概率符合count参数.  
            例如:  
            scan 0 match k1* count 10    :   开始迭代,返回匹配k1的数据,期望返回10条.cursor为0表示刚开始迭代.  
            返回值:  
            1)"115379"					游标  
            2)1) "k1323454"				匹配到的key  
              2) "k1454365"  
              3) "k1546763"  
            scan 115379 match k1* count 10    :  将查询到的cursor再次传入redis查询  
            可能会获取到重复的key,需要我们在外部去重,比如将查询到的结果放入HashSet里面.  
            代码参考 : https://blog.csdn.net/zhxdick/article/details/78268027

   <h3 id="如何通过redis实现分布式锁">如何通过redis实现分布式锁</h3>   
   
   * 分布式锁:控制分布式系统或者不同系统之间共同访问共享资源的锁的实现.     
        * 互斥性   
        * 安全性 : 锁只能被持有该锁的客户端删除,不能被其他客户端删除.   
        * 死锁 : 获取锁的客户端,因为某些原因宕机,而未能释放锁,其他客户端无法获取该锁而导致死锁.   
        * 容错 : 部分redis节点宕机之后,客户端仍然能够获取锁及释放锁.  

   * 如何实现:   
        * 一种思路(有问题):   
                用 setnx key value , 如果key不存在,set成功,返回值为1,如果key存在,set失败,返回值为0.当返回值是1时,用expire给key设定一个时间,并进行task任务,当返回值是0时,表示该资源被占用,不进行task任务.   
                伪代码:   
                <pre>
                    long status = redisService.setnx(key , "1");   
                    if(status = 1){   
                        redisService.expire(key , expireTime);
                        // 执行占用资源的逻辑.
                        doTask();
                    }
                </pre>
                这里的问题是: setnx与expire不是原子性的,如果setnx完之后程序挂了来不及expire,那么资源会被一直锁上,别的程序无法使用.   

        * 另一个思路:   
                通过 set key value [EX seconds] [PX millseconds] [NX|XX] ,原子性操作   
                    EX second : 设置过期时间为second秒.   
                    PX millsecond : 设置键的过期时间为millsecond毫秒.   
                    NX : 只在键不存在时,才对键进行设置操作   
                    XX : 只在键已经存在时,才对键进行设置操作.  
                    SET操作成功完成后,返回OK,否则返回nil.  
                伪代码:  
                <pre>
                    String result = redisService.set(lockKey , requestId , SET_IF_NOT_EXIST, SET_WITH_EXPIRE_TIME , expireTime);
                    if ("OK".equals(result)){
                        // 执行占用资源的逻辑.
                        doTask();
                    }
                </pre>   
         可参考示例代码.
   * 大量的key同时过期的注意事项:   
        key集中过期,redis清除大量key会很耗时,出现短暂卡顿现象.   
        解决方案: 在设置key的过期时间时,给key加上一个随机值.避免集中过期.   
        
   <h3 id="如何使用Redis做异步队列">如何使用Redis做异步队列</h3>          
        
   * 使用List作为队列,RPUSH生产消息,LPOP消费消息.   
        * 给队列中添加元素: rpush testlist aaa   
        * 逐条弹出队列里的信息: lpop testlist   
        * 缺点:没有等待队列里有值就直接消费   
        * 弥补:可以通过在应用层引入Sleep机制去调用LPOP机制.或者用BLOPL key [key...] timeout 阻塞直到有消息到来或者超时.   
         	    例如: blpop testlist 30    
        * 生产一次供多个消费者消费:    
         	pub/sub: 主题订阅者模式    
         	例如: subscribe myTopic  (订阅myTopic频道,无需事先定义频道)    
         		  publish myTopic "hello" (向topic里发信息)    
   
   
   <h3 id="Redis如何做持久化">Redis如何做持久化</h3>   
         
   * RDB(快照持久化): 保存某个时间点的全量数据快照.    
   
        * 配置:在redis.conf文件中:   
         
            1.    
             save 900 1    (在900s之内有1条写入就备份)    
             save 300 10   (在300s之内有10条写入就备份)    
             save 60 10000	(在60s之内有10000条写入就备份)    
             reids每个时段的读写请求都是不同的,为了平衡性能和数据安全的需要,需要根据自身redis得到情况进行合理配置多种策略.    
             
            2.    
             stop-writes-on-bgsave-error yes    
             当备份进程出错时,主进程就停止写入操作,为了保障持久化数据一致性的问题.    
            3.   
             rdbcompression no    
             在备份时,将rdb文件做压缩之后再缓存.建议关闭,因为带来更多CPU消耗.    
             备份文件保存在redis根目录的src文件下,dump.rdb.   
   
        * 主动触发持久化指令:       
         SAVE:阻塞Redis的服务进程,直到RDB文件被创建完毕.    
         BGSAVE:Fork出一个子进程来创建RDB文件,不阻塞服务器进程.    
         可以通过定时任务定期调用BGSAVE命令来备份RDB文件,并按照不同时间戳来存储:   
         lastsave发现时间变化了--> mv dump.rdb dumpxxxx.rdb   
   
        * 自动触发RDB持久化的方式:   
          1. 根据redis.conf配置里的SAVE m n 定时触发(用的是BGSAVE)      
          2. 主从复制时,主节点自动触发   
          3. 执行Debug Reload时   
          4. 执行Shutdown且没有开启AOF持久化   
   
        * BGSAVE的原理:   
           调用系统fork,创建一个子进程,实现Copy-on-Write (COW写时复制).父进程继续处理client请求,子进程负责将内存内容写入临时文件中,此时父子进程会共享相同的物理页面,当父进程处理写请求时,OS会为父进程要修改的页面创建副本,而不是写共享的页面,所以子进程保存的数据是fork时刻的数据.   
            * Copy-on-Write:   
              如果多个调用者同时要求相同资源,它们会共同获取相同的指针指向相同的资源,直到某个调用者试图修改资源时,系统才会真正复制一份副本给该调用者,而其他调用者所见到的最初的资源仍然保持不变.并在新数据写入完成后更新读指针.提升读写并发效率.   
   
        * RDB持久化缺点:    
           1. 内存数据的全量同步,数据量大会由于I/O而严重影响性能.    
           2. 可能会因为Redis挂掉而丢失从当前至最近一次快照期间的数据.  
   
   * AOF(Append-Only-File)持久化:    
        1. 记录下除了查询以外的所有变更数据库状态的指令    
        2. 以append的形式追加保存到AOF文件中.     
        * 配置: redis.conf中      
         appendonly yes        (开启AOF)   
         appendfsync everysec  (每隔一秒将缓存区的内存写入AOF)   
         重启以后在客户端: config set appendonly yes   
   
        * 随着写操作的不断增加,AOF文件会越来越大.     
         redis可以在不中断AOF的前提下,在后台重写AOF文件,原理:  
          1. 调用fork(),创建一个子进程.   
          2. 子进程把新的AOF写到一个临时文件里,把当前的内存数据直接生成命令,并不需要读取老AOF进行分析.   
          3. 主进程持续将新的变动同时写到内存和原来的AOF里.    
          4. 主进程获取子进程重写AOF的完成信号,往新的AOF同步增量变动.  
          5. 使用新的AOF文件替换掉旧的AOF文件.    
          主动触发: bgrewriteaof 指令   
          自动触发配置: ...  
   
        * redis数据的恢复:   
           RDB文件和AOF文件共存情况下的数据恢复流程:   
           重新启动redis,如果有aof文件,直接加载aof文件忽略rdb文件,如果没有aof,再来加载rdb文件.   
   
   * RDB和AOF的优缺点   
        * RDB:   
           优点: 全量数据快照,文件小,恢复快   
           缺点: 无法保存最近一次的快照之后的数据   
        * AOF:   
           优点: 可读性高,适合保存增量数据,数据不易丢失  
           缺点: 以redis命令的形式存储,文件体积大,恢复时间长  
   
        * RDB-AOF混合持久化方式   
           redis的4.0之后推出的混合持久化方式,并且作为默认配置.   
           BGSAVE做镜像全量持久化,AOF做增量持久化   
           先以RDB格式写入全量数据,再以AOF方式写入增量数据.从而减少文件的大小,也不会丢失数据.   
   
   <h3 id="使用Pipeline的好处">使用Pipeline的好处</h3>     
 
   * 通过pipeline一次性传入多条指令(比如2000w)去批量执行,节省多次IO往返的时间,为一次的时间.
   
   
   <h3 id="Redis的读写分离同步机制">Redis的读写分离同步机制</h3>  
   
   写操作在master上进行,读操作在slave上进行.   
   *  主从同步: 最终一致性
   		*	全量同步的过程:  
   			    1. 主节点做一次bgsave,并同时将后续修改操作记录到内存buffer.   
   				2. 主节点完成后将rdb文件全量同步到从节点.从节点加载rdb文件.  
   				3. 从节点加载完成后,再通知主节点将期间增量数据同步到从节点上.   
   
   		*	主从正常运行时增量同步的过程:    
   				1. master接收到用户的操作指令,判断是否需要传播到Slave.    
   				2. 将操作记录追加到AOF文件.  
   				3. 将操作传播到其他Slave: 1)对齐主从库  2)往响应缓存写入指令    
   				4. 将缓存中的数据发送给Slave 
   
   * 解决主从模式master宕机后服务不可用的问题:   
   	    利用Redis Sentinel(redis哨兵) , 它是一个独立的进程,监控多个master-slave集群,发现master宕机之后可以自动进行切换.包括如下功能:   
   		1. 监控: 检查主从服务器是否运行正常.   
   		2. 提醒: 通过API向管理员或者其他应用程序发送故障通知.  
   		3. 自动故障迁移: 主从切换(将失效的master下的slave升级为master)  
   
   * 流言协议Gossip:  
   		1. 每个节点都随机与对方通信,最终所有节点的状态打成一致.  
   		2. 种子节点定期随机向其他节点发送节点列表以及需要传播的消息.  
   		3. 不保证信息一定会传递给所有的节点,但是最终会趋于一致.  
   		区块链利用Gossip进行点对点的去中心化.   
   
   *	主从模式，主负责写，从节点负责读，怎么保证一定能从从节点读到最新的数据呢？如果读的时候刚好在写呢？     
   		这个保证不了，有这种強一致的需求的话建议还是从主库读，毕竟都会有延迟的。或者用dbproxy框架，有些dbproxy框架会把刚写进去又读的放到一个mysql connection里，这样来保证读写一致。   
   
   
   <h3 id="如何将不同的key均匀放在不同的redis集群节点">如何将不同的key均匀放在不同的redis集群节点</h3>     
   
   * redis集群:   
   将不同的key通过某个规则分散存储在多个redis节点上,即数据分片.redis-client采用无中心结构,每个节点都和其他节点连接,采用Gossip协议传播信息和发现新的节点.
      
   * 如何将不同的key均匀放在不同的redis集群节点
   
       * 获取key的hash值,然后对节点数量取模,来对应分配节点.缺点:当我们要动态地增减节点,会导致大量的key无法被命中.为解决这个问题,引入一致性哈希算法.
            *  一致性哈希算法:    
       		  	* 对2^32取模,将哈希值空间组成虚拟的圆环.按顺时针组织,圆环的正上方为0,0点右侧的第一个点为1,0点左侧的第一个点为(2^32-1)
       		  	* 选用服务的ip或者主机名作为关键字,来进行hash,来确定每台服务器在hash环上的位置.将key采用与服务器相同的hash函数来计数hash,确定key在环上的位置,然后顺时针行走第一个遇到的节点即为目标存储服务器. (见图)
       		  	
       		    ![用key计算在环上的位置.png](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/%E7%94%A8key%E8%AE%A1%E7%AE%97%E5%9C%A8%E7%8E%AF%E4%B8%8A%E7%9A%84%E4%BD%8D%E7%BD%AE.png "用key计算在环上的位置.png")
       		    
       		  	* 好处: 对服务器的增减只需重新定位一小段数据.比如C宕机,只有C那段数据会受影响,C段的数据会重新定位到D上. 新增服务器,同理.
   
       		*  哈希环的数据倾斜问题: (见图)    
       		  	* 在节点很少时会因为节点分布不均匀而造成大量数据集中缓存到某一台服务器上.    
       		  	
                ![哈希环的数据倾斜问题.png.png](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/%E5%93%88%E5%B8%8C%E7%8E%AF%E7%9A%84%E6%95%B0%E6%8D%AE%E5%80%BE%E6%96%9C%E9%97%AE%E9%A2%98.png "哈希环的数据倾斜问题.png.png")
                
       		*  引入虚拟节点解决数据倾斜问题: (见图)  
       		
       		    ![引入虚拟节点解决数据倾斜问题.png.png](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/%E5%BC%95%E5%85%A5%E8%99%9A%E6%8B%9F%E8%8A%82%E7%82%B9%E8%A7%A3%E5%86%B3%E6%95%B0%E6%8D%AE%E5%80%BE%E6%96%9C%E9%97%AE%E9%A2%98.png "引入虚拟节点解决数据倾斜问题.png.png")
       		
       		    * 为每台服务器计算虚拟节点,均匀分布到环上,多了一步虚拟节点到实体节点的映射,数据定位算法不变.这样相对较少的数据节点也能实现数据的均匀分布.
       		  	* 实际应用中将虚拟节点设置为32.  
   
   

<br>

<h2 id="Linux">Linux</h2>

<br>
   

   <h3 id="Linux的体系结构">Linux的体系结构</h3>      
 
   ![Linux的体系结构.png](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/Linux%E7%9A%84%E4%BD%93%E7%B3%BB%E7%BB%93%E6%9E%84.png "Linux的体系结构.png")   
   
   * 体系结构分为用户态和内核态:
		* 内核: 本质是一段管理计算机硬件设备的程序.
		* 系统调用: 内核的访问接口,是一种不能再简化的原子性操作.
		* 公用函数库: 系统调用的组合拳.
		* shell: 本质是命令解释器,下通系统调用,上通应用程序.   
			 比如:ls -lrt --> 在默认路径下找到ls的执行文件,并且将附带参数-lrt传入这个文件里面执行.   
		     echo $SHELL  --查看当前版本的shell     
		     cat /etc/shells  --查看本机器支持的shell版本   
		     
   <h3 id="查找特定的文件">查找特定的文件</h3>   

   * 语法: find path [options] params
	    
	    1. find ~ -name "target.java"     --在用户目录下查找文件(~可省略)
	    2. find / -name "target.java"     --在根目录下查找文件
	    3. find ~ -name "target.java"     --模糊查找文件
	    4. find ~ -iname "target*"        --不区分文件名大小写去查找文件.    

	     cd ./karl   "./"代表当前目录下     
	     cd  /karl   "/"代表根目录下   
 
   <h3 id="根据文件内容去筛选">根据文件内容去筛选</h3>     

   * 语法: grep [options] pattern file  
		* 作用: 查找文件里符合条件的字符串的行,支持正则表达式.    
	    * grep "java" target*   --查找target打头的文件夹下的包含java文本的行    

   * 管道操作符 |  
	    * 作用: 可将指令连接起来,前一个指令的输出作为后一个指令的输入   
	    * find ~ | grep "target"   --将"find ~"的输出结果作为grep "target"的输入参数.即在home下所有文件名查包含target的文件. 相当于 find ~ -name "target*"
	    * 管道注意的要点:   
	    	1. 只处理前一个命令正确输出,不处理错误输出.
	    	2. 右边命令必须能够接受标准输入流,否则传递过程中数据会被抛弃.
	    	3. 常用的接收数据管道的命令: sed,awk,grep,cut,head,top,less,more,wc,join,sort,split等.    

	    * 实现日志筛选功能 
	       1. grep 'partial\[true\]' bsc-data.info.log     在log文件里查出"partial[true]"的日志([]需要转义)   
	       2. grep -o 'engine\[[0-9a-z]*\]'   将-o上一步的输出结果作为输入结果,进一步筛出engine信息.    
	       grep 'partial\[true\]' bsc-data.info.log | grep -o 'engine\[[0-9a-z]*\]'   
	       3. grep -v "grep"        -v过滤掉包含"grep"的结果   
	       grep 'partial\[true\]' bsc-data.info.log | grep -o 'engine\[[0-9a-z]*\]' | grep -v "grep" 

   <h3 id="对文件内容做统计">对文件内容做统计</h3>   
   
   * 语法: awk [options] 'cmd' file     awk特别适合处理一些表格里的数据      
        1. 一次读取一行文本,按输入分隔符进行切片,切成多个组成部分
        2. 将切片直接保存在内建的变量中,$1,$2...($0表示行的全部)
        3. 支持对单个切片的判断,支持循环判断,默认分隔符为空格  
   * 例如:
       1. awk '{print $1,$4}' netstat.txt      筛出文件里某些列的数据    
    --netstat.txt文件中,将每一行数据按空格分片,过滤出每一行分片中第一片和第四片的信息.刷选文件可以是多个,只需按空格传入文件即可.
       2. awk '$1=="tcp" && $2==1 {print $0}' netstat.txt       依据一些条件来筛选某些列   
    --过滤出netstat.txt文件中满足每组分片,第一个分片="tcp"以及第二个分片="1"的信息.    
       3. 如果想要过滤的信息中带有表头:  
            NR==1 默认读取的数据行数是1       
            awk '($1=="tcp" && $2==1) || NR==1 {print $0}' netstat.txt   
       4. awk -F "," '{print $2}' test.txt   --  -F ","以","做为分隔符
       5. awk '{enginearr[$1]++}END{for(i in enginearr)print i "\t" enginearr[i]}'   
           对内容逐行统计操作,并列出统计结果.
           定义一个数组enginearr[],用它的下标保存引擎的名字,一旦有相同名字名字的引擎出现,就在原来的基础上累加作为数组元素的值;END{}扫描结束后进行的操作,结束之后遍历enginearr数组,将数组下标和对应的值打印出来.得到engine的名称和其对应出现的次数.
		      
   * grep过滤数据形成一些表格化的数据,再由awk来处理.   
          grep 'partial\[true\]' bsc-data.info.log | grep -o 'engine\[[0-9a-z]*\]' | awk '{enginearr[$1]++}END{for(i in enginearr)print i "\t" enginearr[i]}'          
          统计了各种engine出现的次数.
          
   <h3 id="批量替换文本内容">批量替换文本内容</h3>             
     
   - 语法 :  sed  [option]  'sed command'  filename
     
       - sed , 全名 : stream editor , 流编辑器 . 适合用于对文本的行内容进行处理
     
       - sed -i 's/^Str/String/' replace.java        将java文件中每行开头的Str替换为String
     
         's/^Str/String/'中 : "s"表示进行字符串操作 , 前两个"/"之间表示要替换的内容 , 后两个"/"之间表示要替换成的内容. "^Str" 表示以Str开头 . "-i" 表示改变文件的内容.
     
       - sed -i 's/\\.$/\;/'  replace.java        将java文件中每行末尾的.替换为;
     
         's/\\.$/\;/'中 :  "\\." 表示对"."进行转义 , "$"表示在每行的末尾 . 同样";"也需要转义 . 
     
       - sed -i 's/Jack/Tom/g'  replace.java          将java文件中的Jack替换为Tom(全文)
     
         第三个"/" 后面加g表示全文的替换 , 如果不加g表示将每行的第一个Jack替换掉.
     
       - sed -i '/Integer/d'  replace.java         将带有Integer的行删掉
     
         "d"表示删除
     
     
<h2 id="JVM">JVM</h2>

<br>

   <h3 id="JVM如何加载class文件">JVM如何加载class文件</h3>   

   ![JVM结构模型.png](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/JVM%E7%BB%93%E6%9E%84%E6%A8%A1%E5%9E%8B.png.jpg)

   - JVM 主要由一下四部分组成
     - Class Loader
       - 依据特定格式 , 加载class文件到内存
     - Runtime Data Area (JVM内存模型)
       - 包括Stack , Heap , Method Area , PC Register , Native Method Stack
     - Execution Engine
       - 对命令进行解析
     - Native Interface
       - 融合不同的开发语言的原生库为java语言所用

   <h3 id="什么是反射">什么是反射</h3>   

   ​	是在运行状态中, 对于任意一个类 , 或者一个对象 , 都能够直到这个类的所有属性和方法 , 这种动态获取信息以及动态调用对象的方法称为java语言的反射机制. 即 把java类中的各种成分一个个映射成java对象 . 

   - 写一个反射的例子(见代码)
     - 通过反射机制可以获取/调用类的私有属性以及私有的方法
     - rc.getDeclaredMethod(...) 可以获取到该类的私有和公有方法 , sayNameAndAge.setAccessible(true);但是不能获取到继承来的方法和实现接口的方法 . 
     - rc.getMethod(...) 不能获取到该类的私有方法 , 可以获取到该类的继承方法和实现接口的方法

   <h3 id="谈谈ClassLoader">谈谈ClassLoader</h3>   

   - ClassLoader主要负责将Class里的二进制数据流装载进系统 , 然后交给java虚拟机进行连接 , 初始化等操作 .

   - ClassLoader的种类

     - BootStrapClassLoader : 由C++编写 , 加载java的核心库java.*

     - ExtClassLoader : java编写 , 加载扩展库javax.*

     - AppClassLoader : java编写 , 加载程序所在目录

     - 自定义ClassLoader : java编写 , 自定义加载 (见代码)

       MyClassLoader --> loadClass --> findClass --> loadClassData --> defineClass

   - 谈谈类加载器的双亲委派机制

     ![类加载器的双亲委派机制](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/%E7%B1%BB%E5%8A%A0%E8%BD%BD%E5%99%A8%E7%9A%84%E5%8F%8C%E4%BA%B2%E5%A7%94%E6%B4%BE%E6%9C%BA%E5%88%B6.jpg)

   - 为什么使用双亲委派机制去加载类

     - 避免多分同样的字节码被重复加载 , 保证内存中只有一份.

   - 何如通过openJDK查看native对应的代码 ?

     openJDK , http://hg.openjdk.java.net/jdk8u/jdk8u/jdk/ , browse/src/share(不依赖于平台部分的代码) /native / java / lang

   <h3 id="类的加载方式">类的加载方式</h3>   

   - 隐式加载 : new  : 通过new生成对象时 , 隐式调用类加载器 , 加载对应的class到JVM中 . 

   - 显示加载 : loadClass , forName等 , 还要通过newInstance来得到类的对象 . 

   - loadClass 和 forName的区别 : 

     - 类的装载过程:

       - 通过ClassLoader加载class文件字节码 , 生成Class对象
       - 链接 : 校验 : 检查加载的class的正确性和安全性

       ​	          准备 : 为类变量( static )分配存储空间并设置类变量初始值

       - 初始化 : 执行类变量赋值和静态代码块

     - Class.forName得到的class是已经初始化完成的 , 适用于加载class时就需要完成初始化的场景 , 比如mysql-connector中的Driver中有一段static的初始化代码段 , 我们需要用forName来加载它 . 

     - Class.loadClass得到的class是还没有链接的(只完成了第一步) . 比如spring的ioc , 在初始化bean时 , 为了加快初始化速度 , 对于bean的加载采用延迟加载lazy-loading , 不执行类中的初始化代码 , 到用到这个类时才进行初始化操作 , 就需要用到loadClass的加载方式.

   <h3 id="Java的内存模型">Java的内存模型</h3>   

   ​	![JVM内存模型](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/JVM%E5%86%85%E5%AD%98%E6%A8%A1%E5%9E%8B.jpg)

   - 程序计数器 , 每个线程都有一个程序计数器 , 只对Java方法计数 . 

   - java虚拟机栈( Stack ) , 里面存储多个栈帧 ,每调用一个方法 , 就在栈中生成一个栈帧 , 每一个方法从调用开始至执行完成的过程，都对应着一个栈帧在虚拟机里面从入栈到出栈的过程，在活动线程中，只有位于栈顶的栈帧才是有效的，称为当前栈帧，与这个栈帧相关联的方法称为当前方法。方法调用结束后 , 栈帧就会被自动释放掉 (不需要通过GC回收), 每个栈帧中包含 : 局部变量表 , 操作栈 , 动态连接 , 返回地址 等

     - 局部变量表 : 包含方法执行过程中的所有变量
     - 操作数栈 : 入栈 , 出栈 , 复制 ,交换 等产生的变量

     执行时按程序计数器的数从大到小压入栈 , 再按从小到大的顺序来执行 . 

     - 递归为什么会引起StackOverFlow异常 ? 

       - 什么是斐波那契函数 ?

         F(0) = 0 , F(1) = 1 , 当你>= 2 时 , F(n) = F( n - 1 ) + F( n - 2 );

       ```java    
        public static int fibonacci(int n) {
               if (n == 0) return 0;
               if (n == 1) return 1;
               return fibonacci(n - 1) + fibonacci(n - 2);
           }
       ```

       - 因为每次递归都会往栈里面压一个栈帧 , 递归过深 , 栈帧超出了虚拟栈的深度 . 

   - 本地 方法栈

     - 与虚拟机栈相似 , 主要作用于native的方法

   - 元空间 (MetaSpace)

     - 放类的加载信息 , 类中的属性和方法
     - java8以后 , 元空间( MetaSpace ) 替换了永久代( PermGen ) , 用来存储class相关信息 , 包括class对象的method以及field , 元空间与永久代均是方法区的实现(方法区只是JVM的一种规范) , java7以后字符串常量池从方法区中移动到了java堆中. MetaSpace 与 PermGen最大的区别是 , 元空间使用的是本地内存 , 而永久代使用的是JVM的内存 . 内存分配更合理 , 不会动不动就出现永久代内存溢出的异常 . 

   - Java堆( Heap )

     - 包括常量池( 放字符串常量, 符号常量)
     - 放 数组 , 类对象.

   <h3 id="JVM三大性能调优参数">JVM三大性能调优参数</h3>  
    
   JVM三大性能调优参数 -Xms -Xmx -Xss的含义    
    
   java -Xms128m -Xmx128m -Xss256k -jar xxx.jar

   - -Xss : 规定了每个线程虚拟机栈( 堆栈 )的大小 .  一般256k足够 .
   - -Xms : 创建时的java堆的初始大小 . 
   - -Xmx : java堆的最大值 . 通常将Xms与Xmx的值设为一样 , 因为堆扩容时会发生内存抖动 , 影响程序稳定 .
   - **那么spring boot 环境下，tomcat的运行模式是哪种**
     - SpringBoot默认是以 `java -Xmx256m -Xss256k -jar xx.jar` 来运行内置Tomcat启动方式默认是NIO (非阻塞IO , 基于IO多路复用技术实现，只需要一个线程或者少量线程，就可以处理大量请求 , 而Tomcat7及以前采用BIO , 阻塞IO ,一个请求就用一个线程来处理 , 不适用于高并发场景)

   <h3 id="Java内存模型中堆和栈的区别">Java内存模型中堆和栈的区别</h3>  
   - 内存分配策略 : 

     - 栈式存储 : 数据区需求在编译时未知 , 运行时模块入口前确定内存大小
     - 堆式存储 : 编译时或运行时模块入口都无法确定内存大小 , 程序运行时才动态分配 . 比如可变长度串和对象实例 . 

   - 联系 : 

     引用对象 / 数组时 , 栈里定义局部变量保存堆中目标的首地址 . 

   - 管理方式 : 

     JVM执行机制可以自动释放栈空间 (方法结束时) , 堆内存需要GC释放 .

   - 分配方式 : 

     栈支持静态和动态分配 , 而堆仅支持动态分配 . 

   - 效率

     栈(Stack数据结构)只支持入栈和出栈的操作 , 效率高 , 但不如堆更灵活 ,堆(双向链表)的优势在于动态分配 . 

   <h3 id="元空间/堆/线程独占部分的联系">元空间/堆/线程独占部分的联系</h3>  

   例如一下代码 : 

   ```java
   public class HelloWorld {
       private String name;
       public void setName(String name) {
           this.name = name;
       }
       public void sayHello() {
           System.out.println("hello " + name);
       }
       public static void main(String[] args) {
           int a = 1;
           HelloWorld hw = new HelloWorld();
           hw.setName("test");
           hw.sayHello();
       }
   }
   ```

   元空间 : 

   Class : HelloWorld - Method : sayHello/setName/main - Field : name

   Class : System

   Java堆 : 

   Object : String( "test" )

   Object :  HelloWorld 

   线程独占 (栈) : 

   局部变量 test , 保存String 对象的引用 .

   局部变量 hw , 保存HelloWorld 对象的引用 .

   局部变量 a , 保存的常量 1 .

   代码的行号

   - 在idea中改变永久代的大小 :

      run --> Edit Configration --> 选定方法 --> VM options --> 输入 -XX:MaxPermSize=6M  -XX:PermSize=6M

     JDK6之后字符串常量池移到堆中了 , 不在永久代里了 . 

   <h3 id="不同版本间intern方法的表现">不同版本间intern方法的表现</h3> 

   JDK6 : 如果s字符串常量池中没有该字符串 , 则将字符串添加进常量池中 , 返回字符串在常量池中的引用 ; 如果字符串常量池中有该字符串 , 则直接返回字符串在常量池中的引用 . 

   JDK6+ : 如果字符串常量池中没有该字符串 , 则将字符串在堆中的引用添加进常量池中 , 返回该引用 ; 如果字符串常量池中有该字符串 , 则直接返回字符串在常量池中的引用 .  如果堆中不存在 , 则在池中创建该字符串并返回其引用 .     

   ```java   
   String s1 = new String("a");
   s1.intern();
   String s2 = "a";
   System.out.println( s1 == s2 );
   
   String s3 = new String("a") + new String("a");
   s3.intern();
   String s4 = "aa";
   System.out.println( s3 == s4 );
   ```

   在JDK6下 : 

   ​	false

   ​	false

   分析:  

   s1 == s2 : "a" 会直接在字符串常量池中创建出来 ,  而new String都是在Java的堆中创建出来的 . 因为字符串常量池中以及有了 , 所以s1.intern()没有效果 ,s1是字符串对象在堆中的地址 , s2是字符串在字符串常量池中的地址 .故 s1 != s2 ;

   s3 == s4 : 在堆中生成"aa"对象 , s3.intern()发现常量池中没有该字符串 , 将"aa"的副本放入常量池(注意此时字符串常量池与堆式独立的)中 , s3是堆中的"aa"对象的地址 , s4是常量池中的"aa"的地址 . 故 s3 != s4 ; 

   ![intern-jdk6](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/intern-jdk6.jpg)

   在JDK6+下 :

   ​	false

   ​	true

   分析 :

   s1 == s2 与上面分析同理;

   s3 == s4 : 在堆中生成"aa"对象 , 字符串常量池中没有"aa" , 将堆中"aa"对象的地址放入常量池中(注意此时常量池也放入堆中了) , s3 是"aa"在堆中的地址 , s4也是堆中的引用 , 故 s3 == s4 ;

   ![intern-jdk7](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/intern-jdk7.jpg)


<br>

<h2 id="GC">GC</h2>

<br>

   <h3 id="Java对象被判定为垃圾的标准是什么">Java对象被判定为垃圾的标准是什么</h3>  

   - 没有被其他对象引用

   <h3 id="判定对象是否为垃圾的算法">判定对象是否为垃圾的算法</h3>  

   - 引用计数算法

     通过判断对象的引用数量来决定对象是否可以被回收 

     - 每个对象实例都有一个引用计数器 , 被引用则 + 1 ,完成引用则 - 1
     - 任何引用计数为0的对象实例可以被当做垃圾收集
     - 优点 : 执行效率高 , 程序执行受影响小
     - 缺点 : 无法检测出循环引用的情况 , 导致内存泄漏

   - 可达性分析算法

     通过可达性算法判断对象的引用链是否可达来决定对象是否可以被回收

     - 从一系列GC root节点作为起始点用可达性算法向下搜索 , 所走过的路径称为引用链(Reference chain) . 如果一个对象不在引用链上 , 会被表明不可达 , 被回收 . 
     - 可以作为GC Root的对象
       - 虚拟机栈中的引用的对象
       - 方法区中的常量引用的对象
       - 方法区中的类静态属性引用的对象
       - 本地方法栈中JNI( Native方法 )的引用对象
       - 活跃线程的引用对象

   <h3 id="垃圾回收的算法">垃圾回收的算法</h3>  

   - 标记-清除算法(Mark and Sweep)   ---- 适用于老年代

     - 标记 : 用可达性算法从root节点开始扫描 , 对可达对象进行标记

       清除 : 对堆内存从头到尾进行线性遍历 , 回收不可达的对象内存

     - 缺点 :  仅对不存活的对象进行处理 , 因此在清除之后会产生大量不连续的内存碎片 , 导致以后无法分配较大的连续内存 , 而提前触发另一次GC.

   - 复制算法 ( Copying ) -- 适用于年轻代

     - 分为对象面和空闲面 , 对象在对象面上创建 , 当对象面的空间用完 , 就将存活的对象从对象面复制到空闲面 , 再将对象面的所有对象内存清除 . 每次都对整个半区进行整体的内存回收 , 无需考虑内存碎片 , 适用于对象存活率较低的场景 , 比如年轻代 . 

       ![复制算法](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/%E5%A4%8D%E5%88%B6%E7%AE%97%E6%B3%95.jpg)

   - 标记- 整理算法 ( Compacting )  -- 适用于老年代

     - 标记 : 用可达性算法从root节点开始扫描 , 对可达对象进行标记

       清除 : 移动所有存活的对象 , 且按照内存地址次序依次排列 , 然后将末端内存地址以后的内存全部回收 . 

     - 解决了内存碎片的问题 , 适用于存活率高的场景 . 

   - 分代收集算法 ( Generational Collector )

     - 按照对象生命周期的不同划分区域以采用不同的垃圾回收算法

     - jdk6/jdk7 

       年轻代 / 老年代 / 永久代

     ![jdk6,7的堆内存划分](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/jdk6%2C7%E7%9A%84%E5%A0%86%E5%86%85%E5%AD%98%E5%88%92%E5%88%86.jpg)

     - jdk8

       年轻代 / 年老代

       ![jdk8堆内存的划分](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/jdk8%E5%A0%86%E5%86%85%E5%AD%98%E7%9A%84%E5%88%92%E5%88%86.jpg)

   <h3 id="分代收集算法(Generational-Collector)">分代收集算法(Generational-Collector)</h3>  

   - GC的分类

     - Minor GC -- 发生在年轻代中的垃圾收集动作 , 采用复制算法

       - 年轻代 : 尽可能快速地收集那些生命周期短的对象

         - Eden区 : 新的对象刚创建时分配在此 . 

         - 两个Survivor区 (一个from区 , 一个to区 , 不断变化的)

           ![年轻代](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/%E5%B9%B4%E8%BD%BB%E4%BB%A3.jpg)

       - 年轻代垃圾回收的过程

         - Eden区空间不足时 , 触发Minor GC . 
         - 将Eden和一块Survivor上的存活对象一次性复制到另一个Survivor上 , 清理掉Eden和一块Survivor的全部对象 , 当Survivor不够用了 , 需要依靠老年代做担保 . 

       - 年轻代对象如何晋升到老年代

         - 存活对象每经过一个GC , 它的年龄就 +１，或年龄超过( -XX:MaxTenuringThreshold 默认为15) , 会被移入老年代 .
         - Survivor区中存放不下的对象 , 会移入老年代. 
         - 新生成的大对象 ( -XX: +PretenuerSizeThreshold 设置对象大小)

       - 常用的调优参数

         - -XX:SurvivorRatio : Eden和Survivor的比值 , 默认 8 : 1
         - -XX:NewRatio : 老年代和年轻代内存大小的比例 , 默认 2 : 1
         - -XX:MaxTenuringThreshold : 对象从年轻代晋升到老年代经过GC次数的最大阈值 . 

     - Full GC

       - 老年代 : 存放生命周期较长的对象 , 用标记-清理算法 / 标记-整理算法 

       - 通常Full GC也会对年轻代进行垃圾回收 . 

         Major GC 要问清楚是指full GC 还是只针对年老代的GC

         Full GC比Minor GC慢 , 执行效率低

       - 触发Full GC的条件

         - 老年代空间不足

         - 永久代空间不足 (JDK7以前)

           所以jdk8用元空间代理永久代 , 减少了Full GC的频率 , 降低了GC负担.

         - CMS GC时出现promotion failed , concurrent mode failure

         - Minor GC晋升到老年代的平均大小大于老年代的剩余空间

         - 调用System.gc(); 这里只是程序员提醒JVM进行GC , 决定权在JVM手里 .

         - 使用RMI来进行RPC或管理JDK应用 , 每小时执行一次Full GC;

   <h3 id="GC中什么是Stop-the-World">GC中什么是Stop-the-World</h3>  

   - JVM由于要执行GC而停止了应用程序的执行 , 除了GC线程外 , 其他线程都处于等待状态 . 
   - 任何一种GC算法中都会发生
   - GC的优化就是要减少Stop-the-world发生的时间来提高程序的吞吐量

   <h3 id="什么是Safepoint">什么是Safepoint</h3>  

   - 是分析过程中对象引用关系不会发生变化的点 , 一旦GC发生 , 让所有的线程跑到安全点再停顿下来 . 
   - 安全点的数量不能太少 , 会增加GC等待的时间 ; 不能太多 , 会增加程序运行的负荷 . 

   <h3 id="JVM的运行模式">JVM的运行模式</h3>  

   - Server : 启动慢 , 长期运行时执行速度快 , 因为Server模式启动的是重量级的虚拟机 , 堆程序采用了更多的优化 .
   - Client :  启动快 , 长期运行时执行速度慢 , Client模式采用的轻量级虚拟机 . 
   - java -version 查看 :   比如 "Server VM"

   <h3 id="常见的垃圾收集器">常见的垃圾收集器</h3>  

   - 垃圾收集器之间的联系

     ![垃圾收集器之间的联系](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/%E5%9E%83%E5%9C%BE%E6%94%B6%E9%9B%86%E5%99%A8%E4%B9%8B%E9%97%B4%E7%9A%84%E8%81%94%E7%B3%BB.jpg)

   - 年轻代常见垃圾收集器

     - Serial收集器 ( -XX: +UserSerialGC , 复制算法 )
       - 单线程收集 , 进行垃圾收集时 , 必须暂停所有的工作线程 (停顿在几十ms到一百ms之间)
       - 简单高效 , Client 模式下默认的年轻代收集器
     - ParNew收集器 ( -XX: +UseParNewGC , 复制算法 )
       - 多线程收集 , 其余的行为特点和Serial收集器一样
       - 单核执行效率不如Serial , 在多核执行才有优势 . (可以与CMS配合)
     - Parallel Scavenge收集器 ( -XX: +UseParallelGC , 复制算法 )
       - 吞吐量 = 运行用户代码时间 / ( 运行用户代码时间 + 垃圾收集时间 )
       - 比起关注用户线程停顿时间 , 更关注系统的吞吐量
       - 在多核执行才有优势 , Server模式下默认的年轻代收集器
       - 优化时配合自适应调节策略 : -XX: +UseAdaptiveSizePolicy 把内存管理的调优任务交给JVM区完成 . 

   - 老年代常见的垃圾收集器

     - Serial Old收集器 ( -XX:+UseSerialOldGC , 标记-整理算法 )

       - 单线程收集 , 进行垃圾收集时 , 必须暂停所有工作线程
       - 简单高效 , Client模式下默认的老年代收集器

     - Parallel Old收集器 ( -XX: +UseParallelOldGC , 标记-整理算法 )

       - 多线程 , 吞吐量优先
       - Parallel Scavenge + Parallel Old 搭配使用 , 适用注重吞吐量和CPU资源敏感的场合

     - CMS收集器 ( -XX: +UseConcMarkSweepGC , 标记-清除算法 )

       - 垃圾回收线程几乎能与用户线程做到同时工作 (一边打扫一边丢垃圾) , 即Stop-the-world尽可能被缩短 , 适用于对停顿敏感 , 并且可以提供更大的内存和CPU(更好的硬件) , 适合有较多存活时间长的对象 .  

       - CMS收集垃圾的过程 :

         1. 初始标记: 会短暂暂停JVM , 只扫描并标记到能够和根对象直接关联的对象 . 

         2. 并发标记 : 并发追溯标记 , 程序不会停顿 .

         3. 并发预清理 : 查找执行并发标记阶段从年轻代晋升到老年代的对象 . 

         4. 重新标记 : 暂停JVM , 扫描CMS堆中的剩余对象

         5. 并发清理 : 清理垃圾对象 , 程序不停顿

         6. 并发重置 : 重置CMS收集器的数据结构

            ![CMS工作流程图](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/CMS%E5%B7%A5%E4%BD%9C%E6%B5%81%E7%A8%8B%E5%9B%BE.jpg)

       - 缺点 : 采用的标记-清除算法 , 会产生不连续的内存碎片 , 当要存储一个较大的对象时 , 会触发GC . 

   - 既能用于年轻代 , 可能用于老年代的收集器

     - G1收集器 (-XX: +UseG1GC , 复制 + 标记-整理算法 )
       - 将整个Java堆内存划分成多个大小相等的Region
       - 年轻代和老年代不再物理隔离 , 不需要在JVM启动时就决定那些Region属于年轻代 , 哪些属于年老代
       - Garbage First收集器的特点
         - 并行和并发 
         - 独立管理整个堆 , 分代收集 
         - 空间整合 (基于标记-整理算法 , 解决内存碎片问题)
         - 可预测的停顿 ( 可以设置停顿时间不超过m毫秒)

   - jdk11正在开发的两个垃圾收集器 : EpsilonGC 和 ZGC

   <h3 id="Object的finalize()方法的作用是否与C++的析构函数作用相同">Object的finalize()方法的作用是否与C++的析构函数作用相同</h3>  

   - 与C++的析构函数不同 , 析构函数调用确定(即在对象离开作用域之后会被delete掉), 而它的是不确定的 . 

   - 将未被引用的对象放置于F- Queue队列 , 并在稍后由一个低优先级的finalize线程去处理 . 

   -  由于是低优先级 , 方法的执行随时可能被终止 . 

   - finalize()的作用是给对象最后一次重生的机会

   - finalize()运行不确定性较大 , 运行代价高 , 不建议使用 

   - 举例 : 

     ```java   
     public class Finalization {
     
         public static Finalization finalization;
     
         @Override
         protected void finalize() {
             System.out.println("into finalize");
             finalization = this;    1
         }
     
         public static void main(String[] args) {
             Finalization f = new Finalization();
             System.out.println("first print: " + f);
             f = null;
             // gc()会调用我们重写的finalize()方法
             System.gc();
             System.out.println("second print: " + f);
             System.out.println(f.finalization);
         }
     }
     ```

     运行结果为:

     > first print: com.guoguo.javaAudition.gc.Finalization@7440e464
     > second print: null
     > into finalize
     > null

     最后一个结果为null , 表明finalize()方法中的finalization = this 没有被执行到该方法就被终止了 . 可以在Sysyem.gc()之后加一个等待 , 让finalize()方法执行完 . 结果为 : 

     > first print: com.guoguo.javaAudition.gc.Finalization@7440e464
     > into finalize
     > second print: null
     > com.guoguo.javaAudition.gc.Finalization@7440e464     
     
   <h3 id="Java中的强引用,软引用,弱引用,虚引用">Java中的强引用,软引用,弱引用,虚引用</h3>    

   - 强引用 (Strong Reference )

      - 最普遍的引用: Object obj = new Object();
      - 抛出OutOfMemoryError终止程序也不会回收具有强饮用的对象
      - 通过将对象设置为null来弱化引用 , 使其被回收

   - 软引用 (Soft Reference )

      - 对象处在有用但非必须的状态

      - 只有当内存空间不足时  , GC会回收该引用的对象的内存

      - 可以用来实现高速缓存

        ```java   
        String str = new String("abc");          // 先强引用声明
        SoftReference<String> softRef = new SoftReference<String>(str);              // 软引用
        
        ```

   - 弱引用 (Weak Reference )

      - 非必须对象 , 比软引用更弱一些

      - GC时会被回收

      - 被回收的概率也不大 , 因为GC线程优先级比较低

      - 适用于引用偶尔被使用且不影响垃圾收集的对象

        ```java   
        String str = new String("abc");
        WeakReference<String> weakRef = new WeakReference<String>(str);           // 虚引用
        
        ```

   - 虚引用 (PhantomReference )

      - 不会决定对象的生命周期

      - 任何时候都可能被垃圾收集器回收

      - 跟踪对象被垃圾收集器回收的活动 , 起哨兵作用

      - 必须和引用队列ReferenceQueue联合使用

        ```java   
        String str = new String("abc");
        ReferenceQueue queue = new ReferenceQueue();
        PhantomReference ref = new PhantomReference(str, queue);
        
        ```

   - 四种引用的比较

   ![java中的四种引用](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/java%E4%B8%AD%E7%9A%84%E5%9B%9B%E7%A7%8D%E5%BC%95%E7%94%A8.jpg)

   <h3 id="引用队列(ReferenceQueue)的作用">引用队列(ReferenceQueue)的作用</h3>  

   - 无实际存储结构 , 存储逻辑依赖于内部节点之间的关系表达
   - 存储关联的且被GC的软引用 , 弱引用以及虚引用




<br>

<h2 id="消息队列">消息队列</h2>

<br>
   
   <h3 id="为什么要引入消息中间件">为什么要引入消息中间件</h3>  

  - 系统解耦

    - 比如系统A，这个系统A会产出一个核心数据，现在下游有系统B,C,D,E需要这个数据。然后如果要是某个下游系统突然宕机了呢？系统A的调用代码里是不是会抛异常？
    - 那系统A的同学会收到报警说异常了，结果他还要去care是下游哪个系统宕机了,这样系统耦合度太严重.就采用MQ中间件来实现系统解耦,系统A就把自己的一份核心数据发到MQ里，下游哪个系统感兴趣自己去消费即可.

  - 异步调用

    - 假设你有一个系统调用链路，是系统A调用系统B，一般耗时20ms；系统B调用系统C，一般耗时200ms；系统C调用系统D，一般耗时2s. 可以将系统D从链路中抽离出去做成异步调用,大幅度提高全链路的性能. 
    - 比如点外卖,创建订单、通知商家、分配骑手,那这个找骑手的过程，是需要一套复杂算法来实现调度的，比较耗时. 就可以把找骑手给你送餐的这个步骤从链路中抽离出去，做成异步化的，哪怕延迟个几十秒，但是只要在一定时间范围内给你找到一个骑手去送餐就可以了。

  - 流量削峰

    - MQ中间件来进行流量削峰。所有机器前面部署一层MQ，平时每秒几百请求大家都可以轻松接收消息。

    - 一旦到了瞬时高峰期，一下涌入每秒几千的请求，就可以积压在MQ里面，然后那一台机器慢慢的处理和消费。

    - 等高峰期过了，再消费一段时间，MQ里积压的数据就消费完毕了。
    
   <h3 id="引入消息中间件之后会有哪些缺点">引入消息中间件之后会有哪些缺点</h3>      

  - 系统可用性降低

    - 一旦引入了MQ中间件，你就必须去考虑这个MQ是如何部署的，考虑如果MQ一旦挂了以后，你的系统有没有备用兜底的技术方案，可以保证系统继续运行下去,即高可用保证方案.

  - 系统稳定性降低

    - 消息会丢失
    - 消息会重复insert
    - 百万消息积压在消费者实例里导致OOM

  - 分布式一致性问题

    - 举个例子，比如说系统C现在处理自己本地数据库成功了，然后发送了一个消息给MQ，系统D也确实是消费到了。但是系统D操作自己本地数据库失败了,系统C成功了，系统D失败了，会导致系统整体数据不一致。

      
   <h3 id="如果消费者接收到消息,完成消息之前宕机怎么办?">如果消费者接收到消息,完成消息之前宕机怎么办?</h3>  

  - 将自动ack关闭, 改为手动ack , 在消费者处理完成后手动提交ack. 一旦MQ发现代表消费者的某个仓储服务实例突然宕机了，而这个仓储服务收到的一些订单消息还没来得及处理，没给自己发送那些消息的ack通知。

    此时，RabbitMQ会自动对这条订单消息重发推送给其他在运行中的仓储服务实例，让其他的仓储服务实例去处理这条订单消息。

   <h3 id="在某次高峰期间MQ中间件故障的情况下的卡死情况">在某次高峰期间MQ中间件故障的情况下的卡死情况</h3>      

  - 我们的核心思路是一旦MQ中间件故障，触发降级机制之后，系统接收到一条请求不是立马写本地磁盘，而是采用**内存双缓冲 + 批量刷磁盘的机制**。

    - 这个内存缓冲实际在设计的时候，分为了两个区域。

    - 一个是current区域，用来供系统写入数据，另外一个是ready区域，用来供后台线程刷新数据到磁盘里去。

    - 每一块内存区域设置的缓冲大小是512kb，系统接收到请求就写current缓冲区，但是current缓冲区总共就512kb的内存空间，因此一定会写满。current缓冲区写满之后，就会交换current缓冲区和ready缓冲区。交换过后，ready缓冲区承载了之前写满的512kb的数据。然后current缓冲区此时是空的，可以继续接着系统继续将新来的数据写入交换后的新的current缓冲区。

      ![内存双缓冲机制](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/mq_%E5%86%85%E5%AD%98%E5%8F%8C%E7%BC%93%E5%86%B2%E6%9C%BA%E5%88%B6.png)

    - 此时，后台线程就可以将ready缓冲区中的数据通过Java NIO的API，直接高性能append方式的写入到本地磁盘文件里。当然，这里后台线程会有一整套完善的机制，比如说一个磁盘文件有固定大小，如果达到了一定大小，自动开启一个新的磁盘文件来写入数据。

    - 但是 , 某一次高峰期，系统请求压力达到了平时的10倍以上 , 瞬时涌入的高并发请求一下将current缓冲区写满，然后两个缓冲区交换，后台线程开始刷新ready缓冲区的数据到磁盘文件里去。结果因为高峰期请求涌入过快，导致ready缓冲区的数据还没来得及刷新到磁盘文件，此时current缓冲区又突然写满了。所有机器上部署的实例全部线程都卡死，处于wait的状态。

    - 解决方法就是对线上系统扩容双段缓冲的大小，从512kb扩容到一个缓冲区10mb。

  <h3 id="如何保证消息中间件里的消息不会丢失? (消息的持久化)">如何保证消息中间件里的消息不会丢失? (消息的持久化)</h3>  

  - 在创建queue时 , 有个参数 , 将其设置为true ,  表示创建的queue是durable的，也就是支持持久化的。

  - 生产者发送消息到MQ的时候，需要定义这条消息也是durable，即持久化的。

  - RabbitMQ的消息持久化，是不承诺100%的消息不丢失的。因为有可能RabbitMQ接收到了消息，但是还没来得及持久化到磁盘，他自己就宕机了，这个时候消息还是会丢失的。需要依靠其他的机制。

  <h3 id="如何保证消息中间件全链路数据100%不丢失">如何保证消息中间件全链路数据100%不丢失</h3>      

  - 有一种重量级的机制，就是**事务消息机制**。采用类事务的机制把消息投递到MQ，可以保证消息不丢失，但是性能极差，经过测试性能会呈现几百倍的下降。

  - **轻量级的confirm机制** (类似消费者的ack机制)

   <h3 id="分析一下消费者手动ack机制保证消息不丢失的底层原理">分析一下消费者手动ack机制保证消息不丢失的底层原理</h3>      

  - delivery tag .  RabbitMQ就会通过自己内部的一个**“basic.delivery”**方法来投递消息到仓储服务里去，让他消费消息。

    投递的时候，会给这次消息的投递带上一个重要的东西，就是**“delivery tag”**，你可以认为是本次消息投递的一个**唯一标识**。

  - channel . 每个消费者从RabbitMQ获取消息的时候，都是通过一个channel的概念来进行的 , 这个channel就是进行数据传输的一个管道 .  delivery tag仅仅在一个channel内部是唯一标识消息投递的。所以说，你ack一条消息的时候，必须是通过接受这条消息的同一个channel来进行。

    ![channel](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/mq_channel.png)

  - 其实这里还有一个很重要的点，就是我们可以设置一个参数，然后就批量的发送ack消息给RabbitMQ，这样可以提升整体的性能和吞吐量。

    比如下面那行代码，把第二个参数设置为true就可以了。   
    

    ```java
    channel.basicAck(
    
    ​            delivery.getEnvelope().getDeliveryTag(), 
    
    ​            true);
    ```

    

  - **仓储服务处理失败时的消息重发** , 某个仓储服务实例处理某个消息失败了，此时会进入catch代码块 , 使用nack操作 , 通知RabbitMQ自己没处理成功消息，然后让RabbitMQ将这个消息再次投递给其他的仓储服务实例尝试去完成调度发货的任务。

    ![try-catch代码](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/mq_%E6%B6%88%E8%B4%B9%E8%80%85_try-catch%E4%BB%A3%E7%A0%81.png)

    

    ```java
    channel.basicNack(
    
    ​            delivery.getEnvelope().getDeliveryTag(), 
    
    ​            true);
    ```

    

  - **RabbitMQ如何感知到仓储服务实例宕机** ???

  - **unack消息的积压问题** ,  对于每个channel而言，其实都有一些处于unack状态的消息。

    - 比如RabbitMQ正在投递一条消息到channel，此时消息肯定是unack状态.
    - 然后仓储服务接收到一条消息以后，要处理这条消息需要耗费时间，此时消息肯定是unack状态.
    - 即使你执行了ack之后，你要知道这个ack他默认是异步执行的，尤其如果你开启了批量ack的话，更是有一个延迟时间才会ack的，此时消息也是unack.
    - 如果RabbitMQ给你的消费者服务实例推送的消息过多过快，比如都有几千条消息积压在某个消费者服务实例的内存中。那么此时这几千条消息都是unack的状态，一直积压着，有可能会导致消费者服务实例的内存溢出？内存消耗过大？甚至内存泄露之类的问题产生？

  - RabbitMQ基于一个**prefetch count**来控制这个unack message的数量。可以通过 **“channel.basicQos(10)” **这个方法来设置当前channel的prefetch count。

    - prefetch count设置过大 , 比如说3000，5000 ,  在高并发大流量的场景下，可能就会导致消费者服务的内存被快速的消耗掉 , 服务宕机，然后大量unack的消息会被重新投递给其他的消费者服务，此时其他消费者服务一样的情况，直接宕机，最后造成**雪崩效应**。
    - prefetch count设置过小 , 比如 prefetch count = 1 .  此时你刚处理完这条消息，然后执行了ack的那行代码，结果不幸的是，ack需要异步执行，也就是需要100ms之后才会让RabbitMQ感知到。在这100ms期间，你的消费者服务啥都没干 , 这不就直接导致了你的消费者服务处理消息的吞吐量可能下降10倍，甚至百倍，千倍 .
    - RabbitMQ官方给出的建议是**prefetch count一般设置在100~300之间。**

  - **总结** : 消费端的代码里，必须考虑三个问题：

    - **手动ack、**
    - **处理失败的nack、**
    - **prefetch count的合理设置**

    这三个问题背后涉及到了各种机制：

    - 自动ack机制

    - delivery tag机制

    - ack批量与异步提交机制

    - 消息重发机制

    - 手动nack触发消息重发机制

    - prefetch count过大导致内存溢出问题

    - prefetch count过小导致吞吐量过低

  <h3 id="消息中间件的生产端如何保证数据不丢失">消息中间件的生产端如何保证数据不丢失</h3> 

  - **保证投递消息不丢失的confirm机制**
    - 生产端（比如订单服务）首先需要开启一个confirm模式，接着投递到MQ的消息，如果MQ一旦将消息持久化到磁盘之后，必须也要回传一个confirm消息给生产端。如果没有接收到confirm消息，那么就说明这条消息半路可能丢失了，此时你就可以重新投递消息到MQ去，确保消息不要丢失。
    - 一旦你开启了confirm模式之后，每次消息投递也同样是有一个delivery tag的，也是起到唯一标识一次消息投递的作用。这样，MQ回传ack给生产端的时候，会带上这个delivery tag。你就知道具体对应着哪一次消息投递了，可以删除这条消息。
    - 如果RabbitMQ接收到一条消息之后，结果内部出错发现无法处理这条消息，那么他会回传一个nack消息给生产端。此时你可以选择重新再次投递这条消息到MQ去。或者另一种情况，如果某条消息很长时间都没给你回传ack/nack，那可能是极端意外情况发生了，数据也丢了，你也可以自己重新投递消息到MQ去。

  ![confirm机制代码](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/mq_confirm%E6%9C%BA%E5%88%B6%E4%BB%A3%E7%A0%81.png)
  

  - **confirm机制投递消息的高延迟性**

    - 一旦启用了confirm机制投递消息到MQ之后，MQ是不保证什么时候会给你一个ack或者nack的。正常情况下，你投递到RabbitMQ的消息都会先驻留在内存里，然后过了几百毫秒的延迟时间之后，再一次性批量把多条消息持久化到磁盘里去。因为要是你来一条消息就写一次磁盘，那么性能会很差 . 

      所以正是因为这个原因，你打开了confirm模式之后，很可能你投递出去一条消息，要间隔几百毫秒之后，MQ才会把消息写入磁盘，接着你才会收到MQ回传过来的ack消息，这个就是所谓**confirm机制投递消息的高延迟性**。

    - 首先，用来临时存放未ack消息的存储需要承载高并发写入，**建议采用kv存储**。kv存储承载高并发能力极强，而且kv操作性能很高。

    - 其次，投递消息之后等待ack的过程必须是异步的，也就是类似上面那样的代码，已经给出了一个初步的异步回调的方式。

      消息投递出去之后，这个投递的线程其实就可以返回了，至于每个消息的异步回调，是通过在channel注册一个confirm监听器实现的。收到一个消息ack之后，就从kv存储中删除这条临时消息；收到一个消息nack之后，就从kv存储提取这条消息然后重新投递一次即可；也可以自己对kv存储里的消息做监控，如果超过一定时长没收到ack，就主动重发消息。

  <h3 id="消息中间件全链路100%数据不丢失(三个方面)">消息中间件全链路100%数据不丢失(三个方面)</h3> 

  1. **生产端如何保证投递出去的消息不丢失**消息在半路丢失，或者在MQ内存中宕机导致丢失，此时你如何基于MQ的功能保证消息不要丢失？
  2. **MQ自身如何保证消息不丢失**起码需要让MQ对消息是有持久化到磁盘这个机制。
  3. **消费端如何保证消费到的消息不丢失**如果你处理到一半消费端宕机，导致消息丢失，此时怎么办？
  
  
  
<br>

<h2 id="Java常用类库">Java常用类库</h2>

<br>

  <h3 id="Error和Exception的区别">Error和Exception的区别</h3> 

   - Error : 程序无法处理的系统错误(与JVM相关 : 系统崩溃, 堆内存空间不足  , 方法调用栈溢出等) , 编译器不做检查 . 
   - Exception : 程序可以处理的异常 , 捕获后可能恢复 . 
   - 总结 : 前者是程序无法处理的错误 , 后者是可以处理的异常 . 
   
  <h3 id="Java的异常体系">Java的异常体系</h3> 

   ![java的异常体系](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/java%E7%9A%84%E5%BC%82%E5%B8%B8%E4%BD%93%E7%B3%BB.png)

   - RunTimeException : 不可预知的 , 程序应当自行避免 . ( 比如空指针 , 数组下标越界 )
   - 非RunTimeException(直接继承Exception , 而不是RunTimeException ) : 可预知的 , 从编译器校验的异常 , 即编译时异常. ( 比如IOException , SQLException , 编译器直接报错的 , 需要try-catch) 
   - 从责任角度来看
     - Error属于JVM需要负担的责任
     - RunTimeException是程序应该负担的责任
     - CheckedException可检查异常是Java编译器应该负担的责任 

  <h3 id="常见的Error以及Exception">常见的Error以及Exception</h3> 

   - RuntimeException
     - NullPointerException -- 空指针异常
     - ClassCastException -- 类型强制转换异常
     - IllegalArgumentException -- 传递非法参数异常
     - IndexOutOfBoundsException -- 下标越界异常
     - NumberFormatException  -- 数字格式异常
   - 非RunTimeException
     - ClassNotFoundException  -- 找不到指定class的异常
     - IOException -- IO操作异常
   - Error
     - NoClassDefFoundError  --  找不到class定义的异常
       - 成因 :
       - 类依赖的class或者jar不存在
       - 类文件存在 , 但是存在不同的域中
       - 大小写问题 , javac编译的时候是无视大小写的 , 很有可能编译出来的class文件就与想要的不同
     - StackOverFlowError -- 深递归导致栈被耗尽而抛出的异常
     - OutOfMemoryError -- 内存溢出异常

  <h3 id="数据结构和算法考点">数据结构和算法考点</h3> 

   ![数据结构考点](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E8%80%83%E7%82%B9.jpg)

   ![算法考点](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/%E7%AE%97%E6%B3%95%E8%80%83%E7%82%B9.jpg)


  <h3 id="Java集合">Java集合</h3> 
  
   - list和set考点![list和set常考考点](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/list%E5%92%8Cset%E5%B8%B8%E8%80%83%E8%80%83%E7%82%B9.jpg)
     - set本质是由Map实现的 , 把元素放入Map中的key , 而value给一个new Onject() . 
     - TreeSet中自然排序 ( 传入的对象实现了Comparable的接口) 的优先级低于客户化排序 (在new TreeSet时在构造方法中传入的Comparator类)

  <h3 id="HashMap/HashTable/ConcurentHashMap的区别">HashMap/HashTable/ConcurentHashMap的区别</h3> 

   - HashMap线程不安全 , 数组 + 链表 + 红黑树
   - HashTable线程安全 , 锁住整个对象 , 数组 + 链表
   - ConcurrentHashMap线程安全 , CAS + 同步锁(将锁细粒度到数组的每个元素上) , 数组 + 链表 + 红黑树

  <h3 id="Java8前后HashMap的区别">Java8前后HashMap的区别</h3> 

   - HashMap(Java8以前) :数组(数组的默认长度是16) + 链表
     - 极端情况下元素key全都落在同一个链表下面 , 性能恶化: 从O(1)变为O(n)
   - HashMap(Java8以后) : 数组 + 链表 + 红黑时
     - 通过一个常量TREEIFY_THRESHOLD 默认为8, 当链表长度大于这个值后 , 转化为红黑树 , 这样性能恶化时的复杂度从 O(n)提高到 O(logn) . 当红黑树因为被删除而元素个数小于UNTREEIFY_THRESHOLD默认为6时 , 红黑树转化为链表以保障效率

  <h3 id="HashMap的put方法">HashMap的put方法</h3> 

   1. 如果HashMap未被初始化过 , 则初始化 . 
   2. 对Key求Hash值 , 然后再计算出数组下标. 
   3. 如果没有碰撞 , 直接放入数组下标对应的元素中 . 
   4. 如果碰撞了 , 以链表的方式链接到后面 . 
   5. 如果链表长度超过阈值 默认8, 就把链表转成红黑树
   6. 如果链表长度低于6, 就把红黑树转回链表
   7. 如果key已经存在就替换旧值
   8. 如果数组满了(容量16*加载因子0.75) , 就需要resize (扩容2倍后重排)

  <h3 id="HashMap如何减少碰撞以提高效率">HashMap如何减少碰撞以提高效率</h3> 

   - 利用一些扰动函数 , 促使元素位置分布均匀 , 减少碰撞几率 . 
   - key值使用final对象 , 并采用合适的equals()和hashCode()方法 . 使用String / Integer这样的包装类作为key是很好的选择 , 因为String是final的 , 并重写了equals和hashCode方法了 , final防止防止放入时和查找时的hashCode不一样.

  <h3 id="HashMap扩容的问题">HashMap扩容的问题</h3>     

   - 多线程环境下就, 调整大小会存在条件的竞争 , 容易造成死锁 . 
   - 扩容后重新分配元素的rehashing是一个比较耗时的过程 . 

  <h3 id="什么是HashTable">什么是HashTable</h3>     

   - 是早期Java类库提供的哈希表的实现
   - 线程安全的 : 涉及到的修改方法 , 使用synchronzie锁住整个对象 . 性能较差 . 

  <h3 id="什么是ConcurrentHashMap">什么是ConcurrentHashMap</h3>     

   - java8之前的实现 :  给数据分段(默认分为16个Segment) , 每个分段Segment都有一把分段锁 . 访问其中一个Segment不影响其他Segment的访问 , 理论上比HashTable的效率提高16倍 .  

   - java8之后的实现 : CAS + synchronize(锁更加细粒化 , 只锁定链表/红黑树的首节点 , 这样只要hash不冲突 , 就不会产生并发冲突 , 效率得到提高) 

      底层数据结构也类似于java8以后的HashMap(数组 + 链表 +红黑树)

   - ConcurrentHashMap的put方法逻辑:

      1. 判断Node[]数组是否初始化 , 没有则进行初始化操作 . 
      2. 通过hash定位数组的索引坐标 , 是否有Node节点 , 如果没有则使用CAS进行添加( 链表的头节点 ) , 添加失败则进入下次循环 . 添加成功 :
      3. 检查到内部正在扩容 , 就帮助它一块扩容 . 
      4. 如果链表/红黑树的头节点 != null , 则使用synchronized锁住该头节点 . 继续对链表/红黑树执行添加操作 . 
      5. 判断链表长度 , 如果大于8 , 将链表结构转换为红黑树 . 

  <h3 id="CountDownLatch和CyclicBarrier的区别">CountDownLatch和CyclicBarrier的区别</h3>     

   - CyclicBarrier是所有线程达到栅栏处 , 才触发执行另外一个预先设置的线程 . 这里子线程在await()之后计数器-1 , 就阻塞住了. 
   - CountDownLatch是让主线程等待一组事件发生后继续执行 . 这里子线程在countDown()之后计数器-1 , 没有被阻塞住 . 
   - Exchanger : 两个线程到达同步点后 , 相互交换数据 . 

  <h3 id="BIO/NIO/AIO的区别">BIO/NIO/AIO的区别</h3>     

   - BIO(Block-IO)是基于流模型实现的 , 意味着其交互方式是同步阻塞的 . 

   - NIO(NonBlock-IO) 是多路复用的 , 同步非阻塞的IO操作 . 

      - 核心 :

        - Channels 

          IO都从channel中开始 , 像流 , 数据可以从Channel进入Buffer , 也可以从Buffer流向Channel . 

        - Buffers

        - Selectors

          允许单线程处理多个Channel . 单线程的轮循机制 , 通过高效定位就绪的channel来决定做什么 . 
          如果同时打开多个Channel , 每个Channel流量又很低 , 使用Selector就会很方便 (Channel需要在selector上注册).      

        ![NIO中Selector,Channel,Buffer](https://raw.githubusercontent.com/guoguo-tju/javaAudition/master/src/main/resources/picture/NIO%E4%B8%ADSelector%2CChannel%2CBuffer.jpg)

   - AIO (Asynchronous IO) :  异步非阻塞IO 

     基于事件和回调机制 , 应用操作直接返回而不会阻塞在那里 ,  当后台处理完成 , 响应线程会调用回调函数 . 
     
   ![BIO,NIO,AIO的对比](C:\Users\guozh\Desktop\imooc\BIO,NIO,AIO的对比.jpg)


  	
