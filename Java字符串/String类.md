                                                     String类

# String类常用方法:

## 构造方法:

String():创建空的字符序列

String(byte[] bytes)使用平台默认的字符集解码指定的byte数组,构造成一个新得String(可以另外再带两个参数,指定数组的开始和结束)

String(char[] value)   同样可以指定数组的开始和结束

String(String original)

## 普通方法:

length() 返回字符串的长度.

getBytes() 使用平台默认字符集将String编码未byte序列,并将结果存储到一个byte数组中

toCharArray()将字符串转换为一个新的字符数组.

contains(CharSequence s)

indexOf(String str) 返回指定子字符串在此字符串中第一次出现处的索引.

subString(int beginIndex)或subString(int begin,int end)返回新的字符串.

equals(Object anObject)

equalsIgnoreCase(String anotherString)不考虑大小写.

compareTo()

charAt(int index)指定下标的字符

toUpperCase()

toLowerCase()

split()分割字符串 [split踩坑](https://blog.csdn.net/yongqi_wang/article/details/88900049?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165076513416780366555569%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=165076513416780366555569&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-3-88900049.142^v9^control,157^v4^control&utm_term=String%E7%B1%BB%E4%B8%ADsplit&spm=1018.2226.3001.4187)





# intern()方法

示例:

```java
String s1 = new String("Java中文社群").intern();
String s2 = new String("Java中文社群").intern();
System.out.println(s1 == s2);// true
```

从 JDK1.7 版本以后，常量池已经合并到了堆中，所以不会复制字符串副本，只是会把首次遇到的字符串的引用添加到常量池中。此时只会判断常量池中是否已经有此字符串，如果有就返回常量池中的字符串引用。













引用:

[JVM中的String](E:\JVM\LearningNotes-master\JVM\1_内存与垃圾回收篇\13_StringTable\README.md)

