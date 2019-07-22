![logo](http://google.github.io/flatbuffers/fpl_logo_small.png) FlatBuffers
===========

[![Join the chat at https://gitter.im/google/flatbuffers](https://badges.gitter.im/google/flatbuffers.svg)](https://gitter.im/google/flatbuffers?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Build Status](https://travis-ci.org/google/flatbuffers.svg?branch=master)](https://travis-ci.org/google/flatbuffers) [![Build status](https://ci.appveyor.com/api/projects/status/yg5idd2fnusv1n10?svg=true)](https://ci.appveyor.com/project/gwvo/flatbuffers)

> 三个数据序列化的候选方案：

Protocal Buffers：强大，灵活，但是对内存的消耗会比较大，并不是移动终端上的最佳选择。

Nano-Proto-Buffers：基于Protocal，为移动终端做了特殊的优化，代码执行效率更高，内存使用效率更佳。

FlatBuffers：这个开源库最开始是由Google研发的，专注于提供更优秀的性能。

> 为什么flatbuffers这么高效？

1.序列化数据访问不经过转换，即使用了分层数据。这样我们就不需要初始化解析器（没有复杂的字段映射）并且转换这些数据仍然需要时间。

2.flatbuffers不需要申请更多的空间，不需要分配额外的对象。

大家都知道JSON是纯文本协议，优点是可读性高，使用简单方便；而正是它的优点造成了它解析费时、解析内存耗费高、及数据量大的问题。在移动场景对性能要求极高的情况下，选择JSON作为通信协议无疑不是最佳。

问题

张三是个java程序员,他写产生数据的程序.李四是个python程序员,他要用python处理张三产生的数据.最直观常用的方法就是张三用java把产生的数据保存成csv或者xml文件,然后李四用python读取csv或xml文件.这没有问题.但现在有一种性能更好的方法,flatbuffers.

作用

可以把flatbuffers理解成一个可执行文件flatc.这个可执行文件可以把表示数据格式的fbs文件转化成c++,java,python...代码.张三擅长使用java,他就用flatc把fbs文件转化成java代码.用转化好的java代码把数据存成flatbuffers的格式.李四用flatc把同样的fbs文件转化成自己熟悉的python代码,李四可以用这份python代码把flatbuffers格式文件中的数据读出来.这就实现了不同语言间传数据.当然这只是一个简单的使用场景.flatbuffers的作用远不只是这些.

**FlatBuffers** is a cross platform serialization library architected for
maximum memory efficiency. It allows you to directly access serialized data without parsing/unpacking it first, while still having great forwards/backwards compatibility.

**Go to our [landing page][] to browse our documentation.**

## Supported operating systems
* Windows
* MacOS X
* Linux
* Android
* And any others with a recent C++ compiler.

## Supported programming languages
* C++
* C#
* C
* Dart
* Go
* Java
* JavaScript
* Lobster
* Lua
* PHP
* Python
* Rust
* TypeScript

*and more in progress...*

## Contribution
* [FlatBuffers Google Group][] to discuss FlatBuffers with other developers and users.
* [FlatBuffers Issues Tracker][] to submit an issue.
* [stackoverflow.com][] with [`flatbuffers` tag][] for any questions regarding FlatBuffers.

*To contribute to this project,* see [CONTRIBUTING][].

## Licensing
*Flatbuffers* is licensed under the Apache License, Version 2.0. See [LICENSE][] for the full license text.

<br>

   [CONTRIBUTING]: http://github.com/google/flatbuffers/blob/master/CONTRIBUTING.md
   [`flatbuffers` tag]: https://stackoverflow.com/questions/tagged/flatbuffers
   [FlatBuffers Google Group]: https://groups.google.com/forum/#!forum/flatbuffers
   [FlatBuffers Issues Tracker]: http://github.com/google/flatbuffers/issues
   [stackoverflow.com]: http://stackoverflow.com/search?q=flatbuffers
   [landing page]: https://google.github.io/flatbuffers
   [LICENSE]: https://github.com/google/flatbuffers/blob/master/LICENSE.txt
