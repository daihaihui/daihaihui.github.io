##  1、java主要特点
- 面向对象
三大特性：封装、多态、继承
- 健壮性
吸收了C++的优点，但去掉了指针、内存申请与释放，添加了GC，内存访问更安全
- 跨平台
通过安装JVM实现跨平台

## 2、环境搭建
**开发环境**（ Java开发人员需要安装JDK。如果仅仅是运行Java程序，那么只需要按照JRE）
- JVM（Java Virtual Machine）:Java虚拟机，用于运行编译好的Java程序
- JRE（Java Runtime Environment）：Java运行环境=JVM+核心内库（常用类：String、日期、数学、集合、IO、网络、多线程等）
- JDK（Java Development kits）：JRE+开发工具（javac.exe,java.exe,javadoc.exe等）

**搭建**

- 安装JDK，window上一键安装就行，linux解压就好
- 配置环境变量JAVA_HOME,目的在于希望在命令行使用javac.exe等工具时，任意目录下都可以找到这个工具所在的目录。
## 3、最简JAVA开发

1.编写代码保存为.java文件
```java
class HelloWorld{
    public static void main(String[] args){
        System.out.print("Hello Java!");
    }
}
```
2.使用javac.exe编辑HelloWorld.java文件为HelloWorld.class文件
```java
// 可用javac -help看看
javac E:\HelloWorld.java
//编译时打印出详细日志
javac -verbose E:\HelloWorld.java
```
3.运行.class文件

当class文件不再当前路径时，需要将累的路径加到classpath中，这样jVM执行时就会去classpath路径下寻找类

```java
java   HelloWorld
java -classpath E:\  HelloWorld
//输出详细日志
java -verbose  -classpath E:\  HelloWorld

```
## 4.注意事项
1.java程序的入口是main方法

main函数不一定在public中，但习惯写在public中  

2.java注释
```java
//注释
/*
多行注释
*/
```
3.编码问题
文件都有编码格式，文件要应对应的编码格式打开、执行才不会出错，程序编译若出现编码问题时可以指定文件的编码格式。

4.大小写问题

- 代码中区分大小写  
- 源文件名**不区分**大小写  
- 字节码文件名与类名区分大小写 

5.源文件名与类名一致问题

- public类必须一致，否则可不一致，建议一致  
- 一个源文件只能有一个public类，每个类会生成一个.class字节码文件  

  

