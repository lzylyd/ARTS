# 请停止使用else关键词

本周 review 的是来自 medium 的文章 [Stop using the ‘else’ keyword in your code](https://medium.com/javascript-in-plain-english/stop-using-the-else-keyword-in-your-code-907e82b3054a) 翻译就暂且不做了,因为 repo 建立的时间比较晚,翻译的时间已经不够了。这篇文章大概是在本周三左右 medium 给我的邮箱发送的推送。

整篇文章是基于 js 进行写作的,各位在平时工作的时候经常写 if...else这样的判断,作者在文章里阐述了一个问题:当你使用大于 2 个条件以上的时候最好不要使用 else 语句，其实最好的情况是不要使用 else 语句，举个栗子:  
```java
//当你使用的是普通的 binary 条件的时候 虽然代码有点丑 但是还是可以勉强看明白
if(foo){
    return foo
}else{
    return bar
}
//但是当条件变多了 情况就糟糕了
if(foo){
    
}else if(bar){
    
}else if(bar2){
    
}
...

```

一般我工作的时候都是对条件判断分别拆分成多个 if  配合注释 可以更好的理解。