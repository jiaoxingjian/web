# computer storage

## 磁盘

- from disk to schedule ,from arch to leetcode 
- [ ] [你的硬盘是如何储存数据的？](https://www.youtube.com/watch?v=svhIPM2VT8U)
- [ ] [Bytes, Arrays, and Pointers | Understanding Memory | Data Structures & Algorithms | JomaClass](https://www.youtube.com/watch?v=fVVrfJM4JeY)
- [ ] [如何为十三亿人调度列车 | 回形针](https://www.youtube.com/watch?v=UR42ruEVZ4E)
- [ ] [如何为14亿人调度飞机？](https://www.youtube.com/watch?v=5ZphSjh1ngU)
- [ ] [磁盘调度算法](https://www.jianshu.com/p/3c2b79af130b)
- [ ] [memory and storage](https://www.youtube.com/watch?v=TQCr9RV7twk&t=397s)
- [ ] [2021王道操作系统之 15 第四章 文件管理15](https://www.youtube.com/watch?v=5QjM_Xccc8A&t=413s)
  ![](https://i.imgur.com/jynRUER.png)
  ![](https://i.imgur.com/O7jLMgi.png)
- [ ] [Raw Drive Recovery: How to Recover Data from RAW Drive with Ease](https://www.easeus.com/datarecoverywizard/recover-raw-drive.htm)
- [ ] [Data Recovery On A 1TB Western Digital Hard Drive](https://www.youtube.com/watch?v=6hQZ09sdcRs)
  ![](https://i.imgur.com/lpRjGXc.png)
  这里边蕴含的商机/ 自家的磁盘的备份

## 文件系统

- [Explaining File Systems: NTFS, exFAT, FAT32, ext4 & More](https://www.youtube.com/watch?v=_h30HBYxtws)

```
fdisk ,mount
```

管理磁盘坏块/空闲块等。

- [ ] [read raw disk data](https://www.google.com/search?q=read+raw+disk+data&oq=read+raw+disk+data&aqs=chrome..69i57j0i5i30l2j0i8i30.7633j0j7&sourceid=chrome&ie=UTF-8)
- [ ] [Clicking hard drive dis-assembly. How to and what to expect. 500GIG Western Digital USB storage.](https://www.youtube.com/watch?v=MU6TZxwyg0w)
  ![](https://i.imgur.com/BPmzvMq.png)
- [ ] [Disk access time , Seek Time ,Latency , Transfer time , RPM - Ali Ghalehbanb](https://www.youtube.com/watch?v=rmthZyG8wko)
  ![](https://i.imgur.com/dgPlExj.png)
- [ ] [How a Hard Disk Drive Works](https://www.youtube.com/watch?v=NtPc0jI21i0)
  ![](https://i.imgur.com/n1uKbJz.png)
- [ ] [磁盘可靠性 raid ](https://www.youtube.com/watch?v=sN3tTkvaJ-k)
- [ ] [CSL 206 :EXP No:11 :C program to implement FCFS DISK Scheduling algorithm](https://www.youtube.com/watch?v=GpBLIhd51Hg)
  ![](https://i.imgur.com/9M1BXMK.png)
  所有算法应该试图通过sort， filter，等这些基本算法来实现。
  所以： 根据当前位置排序所有的下面操作。此排序fcfs等。
      根据排序结果来操作。
  引入c++的algorithm。
- [ ] 

## 数据库

- [ ] [sqlbolt](https://sqlbolt.com/lesson/select_queries_introduction)

数据文件独立出来，成为数据库， 对外提供服务。

## 源码分析
- [ ] [leveldb源码分析  GitHub](https://github.com/balloonwj/CppGuide/blob/master/articles/leveldb%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90/leveldb%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%906.md)
- [ ] [rocksdb源码分析]()
- [ ] [cockroachDB源码分析]()
## 行业
- [ ] [Igor Canadi + Mark Callaghan - RocksDB The Databaseology Lectures - CMU Fall 2015](https://www.youtube.com/watch?v=jGCv4r8CJEI)
- [ ] [字节跳动在 RocksDB 存储引擎上的改进实践](https://www.infoq.cn/article/u3leu3emgjjwflqltjhs)
- [ ] [Why we built CockroachDB on top of RocksDB](https://www.cockroachlabs.com/blog/cockroachdb-on-rocksd/)
- [ ] [RocksDB Is Eating the Database World](https://rockset.com/blog/rocksdb-is-eating-the-database-world/)
![](https://hackmd.io/_uploads/B1zokkSc3.png)
![](https://hackmd.io/_uploads/rk5Zl1Hc3.png)
![](https://hackmd.io/_uploads/rJjPXBH5h.png)
![](https://hackmd.io/_uploads/BJ6HNSHcn.png)

## 基础知识
- [x] [红黑树 数据库 ](https://www.cnblogs.com/yufeng218/p/12465694.html)
- [ ] [红黑树 数据库 4k 分页](https://cloud.tencent.com/developer/article/1605594 )
- [ ] [红黑树 数据库 4k 分页 加锁](https://blog.csdn.net/qq_36565596/article/details/107895579)
![](https://hackmd.io/_uploads/S1Jtvj4c2.png)
![](https://hackmd.io/_uploads/S1wLOoVc2.png)

- [ ] [sstable设计](https://www.cnblogs.com/fxjwind/archive/2012/08/14/2638371.html)
```
分析上述只是对于常用数据库的操作是够用的。
表的join，顺次拿到各个表的读锁。
表的update，拿到表的写锁即可。
表应该还有自己的缓存。
表的隔离级别，每个sql 执行过程的所有中间过程对其他sql过程
- 完全隔离 看不到  对比k8s的多租户
- 不隔离 看到脏数据
```
- [ ] [Innodb中的事务隔离级别和锁的关系](https://tech.meituan.com/2014/08/20/innodb-lock.html)
![](https://i.imgur.com/0apr4Xe.png)

- [ ] [rocksdb](http://alexstocks.github.io/html/rocksdb.html)
```
将数据形成Log-Structured：在将数据写入LSM内存结构之前，先记录log。这样LSM就可以将有易失性的内存看做永久性存储器。并且信任内存上的数据，等到内存容量达到threshold再集体写入磁盘。将数据形成Log-Structured，也是将整体存储结构转换成了“内存(in-memory)”存储结构。
将所有磁盘上数据不组织成一个整体索引结构，而组织成有序的文件集：因为磁盘随机读写比顺序读写慢3个数量级，LSM尽量将磁盘读写转换成顺序读写。将磁盘上的数据组织成B树这样的一个整体索引结构，虽然查找很高效，但是面对随机读写，由于大量寻道导致其性能不佳。而LSM用了一种很有趣的方法，将所有数据不组织成一个整体索引结构，而组织成有序的文件集。每次LSM面对磁盘写，将数据写入一个或几个新生成的文件，顺序写入且不能修改其他文件，这样就将随机读写转换成了顺序读写。LSM将一次性集体写入的文件作为一个level，磁盘上划分多level，level与level之间互相隔离。这就形成了，以写入数据时间线形成的逻辑上、而非物理上的层级结构，这也就是为什么LSM被命名为”tree“，但不是“tree”。
将数据按key排序，在合并不同file、level上的数据时类似merge-join：如果一直保持生成新的文件，不仅写入会造成冗余空间，而且也会大量降低读的性能。所以要高效的、周期性合并不同file、level。而如果数据是乱序的，根本做不到高效合并。所以LSM要将数据按key排序，在合并不同file、level上的数据时类似 merge-join。
```

- [ ] [LSM-Tree 的写放大写放大、读放大、空间放大RockDB 写放大简单分析参考文档](https://cloud.tencent.com/developer/article/1352666)

- [ ] [RocksDB Tuning Guide](https://github.com/facebook/rocksdb/wiki/RocksDB-Tuning-Guide)

- [ ] [python扩展rocksdb的时序zset数据结构](http://xiaorui.cc/archives/4406)

- [ ] [为什么我们在 RocksDB 之上构建 CockroachDB](https://www.cockroachlabs.com/blog/cockroachdb-on-rocksd/)

  ![image-20230723191204908](.\Img\image-20230723191204908.png)

  ![image-20230723191241736](.\Img\image-20230723191241736.png)

![image-20230723191432222](.\Img\image-20230723191432222.png)

## file system

- [ ] [漫谈linux文件IO](https://zhuanlan.zhihu.com/p/424507991)
- [ ] [Linux: What can you epoll?](https://darkcoding.net/software/linux-what-can-you-epoll/)
```
Network sockets
Timers
Signals
Filesystem events
Child processes
Terminals
Page faults
Seccomp notifications
Epoll inception
POSIX message queues:
UNIX socket pairs
Pipes (or FIFOs aka named pipe): man 7 pipe.
eventfd: 
And what you can’t epoll: regular files
Calling epoll_ctl with a regular (disk) file will return error EPERM:

Linux does have two facilities for true async disk I/O: libaio and io_uring. Neither of them give you file descriptors you can epoll. They could be integrated thanks to eventfd, or io_uring could become the event loop and control the epoll fd via io_uring_enter’s IORING_OP_EPOLL_CTL.
```
- [ ] [Epoll on regular files](https://stackoverflow.com/questions/8057892/epoll-on-regular-files)
- [ ] [Asynchronous file I/O on Linux: the epoll API](https://daankolthof.com/2019/08/01/asynchronous-file-i-o-on-linux-the-epoll-api/)

what i do if i write rocksdb from scratch.

- [ ] [Write a time-series database engine from scratch - Ryo Nakao](https://nakabonne.dev/posts/write-tsdb-from-scratch/)
- [ ] [LevelDB written in Go: Build from scratch?](https://forum.golangbridge.org/t/leveldb-written-in-go-build-from-scratch/4431](https://forum.golangbridge.org/t/leveldb-written-in-go-build-from-scratch/4431)

## 存储服务器

- [数据中心](https://lh3.googleusercontent.com/AqYG_1icmEnnBQFWiwZDrxNxJu6W_Up3Qbzsnw2MYGk5gbwiRG0-vZTlbDaWtOhvdWdNRNDFZZY5tdgoKB4123O_69HB73j-SKV95iY=w600-l100-sg-rj-c0xffffff)

  
