# Java 代码的基本元素

```java
/*
An example
*/
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

> 不过鉴于Java会处理Unicode转义，所以这段代码：
>
> ```java
> int a = 114514; // \u000d a = 1919810;
> System.out.println(a);
> ```
>
> 在javac的视角下是这样的：
>
> ```java
> int a = 114514; // 
> a = 1919810;
> System.out.println(a);
> ```

## 2. 标识符 Identifiers

标识符在代码中是名字的作用。如上的片段中出现了这些标识符：

- `Example`
- `main`
- `args`
- `a`
- `b`
- `System`，`out`，`println`

这些标识符的命名遵循如下的规则：

