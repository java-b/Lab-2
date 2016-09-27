#Lab2
#课程目标：

>首先了解作用域的概念，然后学习字符串的操作以及条件判断的使用，最后利用所学完成一个小程序。



#作用域

>通常来说，一段程序代码中所用到的名字并不总是有效/可用的，而限定这个名字的可用性的代码范围就是这个名字的作用域。

>案例分析：

>```
if(true){
  int a = 1;
}
System.out.println(a);
```

>这是一段错误的代码，如果不清楚原理的同学，可以放在main函数中运行。

>原因就是 a 定义在 if 中，作用域也仅仅于此，出了这里便无效了。

>而要做到：在条件语句中得到某个值，然后在外面打印。可以这样实现：

>```
int a;
if(true){
  a = 1;
}
System.out.println(a);
```
>在这里， `int a;` 对a进行了声明，而 ` a = 1 ;` 对a进行了赋值。 

#字符串操作

##字符串截取

>常用的`字符串截取`操作调用的函数为 `s.substring(int beginIndex, int endIndex)`,

>效果为截取从 beginIndex 至 endIndex 的字符串，包括beginIndex的字符，不包括endIndex的字符。

>比如：` String s = "12345";System.out.println(s.substring(1,3));`，打印结果为 `23`.

>即`[beginIndex,endIndex)`,左开右闭。

>如果是要获得`某个特定位置`的字符，也可以使用`s.charAt(int index)`。

##字符串转换

>比如我们现在得到一个数字组成的字符串`12345`,如何将他转换成数字呢？

>我们可以通过刚才讲述的字符串截取逐个获取数字，然后拼凑出整个数字。

>而在我们确定这是一个整数的前提下，我们可以调用`Integer.parseInt(String s)`。

>类似的，也有`Double.parseDouble(String s)`。

#条件判断

>首先放比较标准的代码:

>```        
        if(expression){
            //code here
        }else if(expreession){
            //code here
        }else{
            //code here
        }
```

>规则非常简单，第一种情况（包括只有一种情况）使用 `if`,最后一种情况使用`else`,其他中间情况使用`else if`。

>注意这里每个`if`后都跟着一对花括号，而在没有花括号时，并不直接算语法错误，而是读取下一行作为执行语句。

>比如:

>```
if(expression)System.out.println("just one line");
```
>是可以运行的。

#计算字符串算式

##要求

>给定一个字符串'x operator y'，x和y是10以内的整数，operator是+,-,\*,/中的一种,打印其结果。

##提示

>1.当除数为0时，会发生什么呢？需给出相应输出。

>2.操作符两边需留出一个空格。

##输入样例

`1 + 1`

##输出样例

`2`


