# Java 代码的基本元素

```java title="An example"
public class Example {
    public static void main(String args[]) {
        int a = 114514;
        int b = 1919810;
        System.out.println("a + b = " + (a + b));
    }
}
```

## 1. 注释 Comments

- 单行注释：以 `//` 开始，作用于其后方的内容
- 长注释：以 `/*` 开始，`*/` 结束

注意：长注释有时也被叫做多行注释，但是实际上并无要求。如下的代码是正确的

```java
int a = 114514; /* Single line comment */
```

注释内部的内容会被全部忽略

!!! note

    不过鉴于Java会处理Unicode转义，所以这段代码：
    
    ```java
    int a = 114514; // \u000d a = 1919810;
    System.out.println(a);
    ```
    
    在javac的视角下是这样的：
    
    ```java
    int a = 114514; // 
    a = 1919810;
    System.out.println(a);
    ```

## 2. 标识符 Identifiers

标识符在代码中是名字的作用。如上的片段中出现了这些标识符：

- `Example`
- `main`
- `String`，`args`
- `a`
- `b`
- `System`，`out`，`println`

这些标识符的命名遵循如下的规则：

1. 不能与关键字重名
2. 只能由数字，字母，美元符号，下划线和大于0xC0的Unicode字符组成
3. 第一个符号**不能是数字**
4. 区分大小写

这些标识符是合法的：

- `中文`
- `length`
- `_length`
- `$mixed`

不合法的标识符会在编译阶段导致错误。

## 3. 关键字 Keywords

关键字可以看作是Java提供的标识符，它们往往具有特殊的含义。

Java的关键字如下：

| 关键字       | 说明                           |
| ------------ | ------------------------------ |
| private      | 私有的                         |
| protected    | 受保护的                       |
| public       | 公共的                         |
| default      | 默认                           |
| abstract     | 声明抽象                       |
| class        | 类                             |
| extends      | 扩充,继承                      |
| final        | 最终值,不可改变的              |
| implements   | 实现（接口）                   |
| interface    | 接口                           |
| native       | 本地，原生方法（非 Java 实现） |
| new          | 新,创建                        |
| static       | 静态                           |
| strictfp     | 严格,精准                      |
| synchronized | 线程,同步                      |
| transient    | 短暂                           |
| volatile     | 易失                           |
| break        | 跳出循环                       |
| case         | 定义一个值以供 switch 选择     |
| continue     | 继续                           |
| default      | 默认                           |
| do           | 运行                           |
| else         | 否则                           |
| for          | 循环                           |
| if           | 如果                           |
| instanceof   | 实例                           |
| return       | 返回                           |
| switch       | 根据值选择执行                 |
| while        | 循环                           |
| assert       | 断言表达式是否为真             |
| catch        | 捕捉异常                       |
| finally      | 有没有异常都执行               |
| throw        | 抛出一个异常对象               |
| throws       | 声明一个异常可能被抛出         |
| try          | 捕获异常                       |
| import       | 引入                           |
| package      | 包                             |
| boolean      | 布尔型                         |
| byte         | 字节型                         |
| char         | 字符型                         |
| double       | 双精度浮点                     |
| float        | 单精度浮点                     |
| int          | 整型                           |
| long         | 长整型                         |
| short        | 短整型                         |
| super        | 父类,超类                      |
| this         | 本类                           |
| void         | 无返回值                       |
| goto         | 是关键字，但不能使用           |
| const        | 是关键字，但不能使用           |

!!!note

	注意区分 **字面常量** 和 **关键字**，以下内容属于字面常量：
	
	 - `"blabla"`
	 - `114514`
	 - `null`，`true`，`false`
	
	字面常量同样也不能用作标识符


## 4. 字面常量 Literal Value

字面常量有时候也被叫做立即值（Immediate）

字面量用来表示由程序员明确指定的值，下面这些都是字面量：

- `1234`
- `"字符串"`
- `'字'`
- `true`

## 5. 运算符 Operators

Java中的运算符可以分为这几类：

- 算数运算符
  - `+`，`-`
  - `*`，`/`
  - `%`
- 关系运算符
  - `==`，`!=`
  - `>`，`<`
  - `>=`，`<=`
- 位运算符
  - `&`，`|`，`^`
  - `~`
  - `<<`，`>>`，`>>>`

- 逻辑运算符
  - `&`，`|`
  - `&&`，`||`
  - `!`
- 赋值运算符
  - `=`
  - `+=`，`-=`，`*=`，`/=`，`%=`，`<<=`，`>>=`，`&=`，`^=`，`|=`
  - `++`，`--`
- 其他
  - `?:`
  - `instanceof`
  - `()`

## 表达式 Expressions

表达式是由上述基本元素组成的，表达式一定能计算出一个值。

下面是一些表达式和它们计算之后的值：

- `1+1` —— `2`
- `true && false` —— `false`
- `1 == 2` —— `false`
- `1+1 == 2 ? 114514 : 1919810` —— `114514`
- `a+b` —— `具体值取决于这两个变量`
- `a++` —— `a的值`
- `++a` —— `a+1的结果`

## 语句 Statements

语句是由表达式和上述基本元素组成的，语句不会有任何计算值。

语句最后一定以分号结尾，下面是一些例子：

- `;` 空语句
- `int a = 114514;` 赋值语句
- `a++;`

用大括号可以把许多语句组合成一个语句，被括起来的代码叫做 **块**

一个普通代码块：

```java
{
    int a = 114514;
    a++;
    System.out.println(a); // 114515
}
```

代码块会影响变量的作用域，如下的代码无法通过编译：

```java
{
    int a = 114514;
    a++;
}
System.out.println(a); // a不存在
```

有关变量作用域的内容会在 *变量和常量* 一节中具体描述。
