# Java语言特点

## Java的基本思想

Java在创建初是为了解决跨平台运行这一问题。过去，将程序移植到不同的操作系统和平台是极为复杂的，需要反复的调试和编译。

Java是 **Java语言** 和 **Java平台** 的总称。无论是在任何操作系统平台上，只需要安装Java平台即可执行某个Java编写的程序。而且在主机上运行的Java平台将程序与环境的交互细节隐藏并封装起来。这一点大大减少了开发难度，真正实现了一次编写，到处运行。

## 技术体系

Java的技术体系包括这几部分：

- Java 编程语言
- Java 类文件格式 `.class`

!!! note

    事实上，这类二进制文件**不一定**必须是由Java语言编译而来的，这种文件格式只是为了让Java虚拟机执行。
    其他JVM语言，如*Kotlin*，*Julia*就可以将自身编译成class文件并在JVM上执行，并可以无缝调用其他JVM语言写成的类库。

- Java API 类库 和 第三方 Java 类库
- 各种平台的Java虚拟机（JVM）

而这些部分又有三种主要版本：

- Java Standard Edition
- Java Enterprise Edition
- Java Micro Edition

这些内容往往以两种工具包提供：

- Java Development Kit
  - JVM
  - Java API 类库
  - Java 开发工具（如编译器和调试分析工具）
  - Java 开发文档和例程
- Java Runtime Environment
  - JVM
  - Java API 基础类库

## 主要特性

- 解释型，动态类型
- 面向对象
- 高性能

