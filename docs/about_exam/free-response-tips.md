# 问答题

## 要求

1. 补全一个方法
2. 补全`class`的`constructor`
3. 撰写一个完整的`class`

全部代码题均由人评审，因此需要保证代码的整洁和规范。

越容易理解的答案越容易得分，但是**无需写任何注释。**

在答题前需要阅读**Examples Table**，确保代码符合要求。

## 知识点

1. Methods & Control Structures

   方法和控制结构（Conditional branches, Loops 和 Branching statements）

2. Class

3. Array/Array List

4. 2D Array

涉及到代码的部分扣分规则（扣一分）：

- 影响正常得分的无关代码

  如题目要求输出某个运算的结果，但是一些语句中途输出了无关内容，则扣分

  ```java
  System.out.println("Calculating..."); // 输出了无关内容
  int answer = 1+1;
  System.out.println(answer);
  ```

- 使用了没有声明的Local variables

  ```java
  int next = some_iter.next(); // 使用了没有声明的some_iter
  System.out.println(next);
  ```

- 变动了persistent data

  ```java
  void do_sth(Map para) { // 这里是引用传递
      para.put(114514, 1919810); // 修改了引用传递
  }
  ```

- 定义了Void的方法（或Constructor）却返回了值

  ```java
  void do_sth() {
      return 114514; // 不应该返回任何值
  }
  ```

涉及到以下内容不会被扣分：

- 无关代码或死代码，但是不影响题目规则

- 为Local variables添加了`private`限定

- 没有为类或constructor添加`public`限定

- 使用数学符号表示运算符（如÷，×）

- 混淆`=`和`==`

- 使用了`[i,j]`而不是`[i][j]`

- 没有为无参数变量添加`()`

  ```java
  void do_sth {
      ...
  }
  ```

- 没有为`if/while`的条件句添加括号

  ```java
  if 1+1==2 {
      ...
  }
  ```

  