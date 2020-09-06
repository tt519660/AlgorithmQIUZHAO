五毒神掌：

第一遍：五分钟读题思考，有思路就直接写，没思路就直接看题解并默写题解 
第二遍：不看题解，自己写代码
第三遍：24小时后 
第四遍：一周后 
第五遍：面试前

字符串个人感悟：
专题刷字符串，理解的深刻。看起来很简单但是比较考验基本功。
老师说，题目不能只过一遍要过多遍。

java中String的常用方法
1、length() 字符串的长度
　　例：char chars[]={'a','b'.'c'};
　　　　String s=new String(chars);
　　　　int len=s.length();

2、charAt() 截取一个字符
　　例：char ch;
　　　　ch="abc".charAt(1); 返回'b'

3、 getChars() 截取多个字符
　　void getChars(int sourceStart,int sourceEnd,char target[],int targetStart)
　　sourceStart指定了子串开始字符的下标，sourceEnd指定了子串结束后的下一个字符的下标。因此， 子串包含从sourceStart到sourceEnd-1的字符。接收字符的数组由target指定，target中开始复制子串的下标值是targetStart。
　　例：String s="this is a demo of the getChars method.";
　　　　char buf[]=new char[20];
　　　　s.getChars(10,14,buf,0);

4、getBytes()
　　替代getChars()的一种方法是将字符存储在字节数组中，该方法即getBytes()。

5、toCharArray()

6、equals()和equalsIgnoreCase() 比较两个字符串

7、regionMatches() 用于比较一个字符串中特定区域与另一特定区域，它有一个重载的形式允许在比较中忽略大小写。
　　boolean regionMatches(int startIndex,String str2,int str2StartIndex,int numChars)
　　boolean regionMatches(boolean ignoreCase,int startIndex,String str2,int str2StartIndex,int numChars)

8、startsWith()和endsWith()　　startsWith()方法决定是否以特定字符串开始，endWith()方法决定是否以特定字符串结束

9、equals()和==
　　equals()方法比较字符串对象中的字符，==运算符比较两个对象是否引用同一实例。
　　例：String s1="Hello";
　　　　String s2=new String(s1);
　　　　s1.eauals(s2); //true
　　　　s1==s2;//false

10、compareTo()和compareToIgnoreCase() 比较字符串

11、indexOf()和lastIndexOf()
　　indexOf() 查找字符或者子串第一次出现的地方。
　　lastIndexOf() 查找字符或者子串是后一次出现的地方。

12、substring()　　它有两种形式，第一种是：String substring(int startIndex)
　　　　　　　　 第二种是：String substring(int startIndex,int endIndex)

13、concat() 连接两个字符串

14 、replace() 替换
　　它有两种形式，第一种形式用一个字符在调用字符串中所有出现某个字符的地方进行替换，形式如下：
　　String replace(char original,char replacement)
　　例如：String s="Hello".replace('l','w');
　　第二种形式是用一个字符序列替换另一个字符序列，形式如下：
　　String replace(CharSequence original,CharSequence replacement)

15、trim() 去掉起始和结尾的空格

16、valueOf() 转换为字符串

17、toLowerCase() 转换为小写

18、toUpperCase() 转换为大写

19、StringBuffer构造函数
　　StringBuffer定义了三个构造函数：
　　StringBuffer()
　　StringBuffer(int size)
　　StringBuffer(String str)
　　StringBuffer(CharSequence chars)
　　
　　(1)、length()和capacity()　　　　一个StringBuffer当前长度可通过length()方法得到,而整个可分配空间通过capacity()方法得到。
　　
　　(2)、ensureCapacity() 设置缓冲区的大小
　　　　void ensureCapacity(int capacity)

　　(3)、setLength() 设置缓冲区的长度
　　　　void setLength(int len)

　　(4)、charAt()和setCharAt()
　　　　char charAt(int where)
　　　　void setCharAt(int where,char ch)

　　(5)、getChars()
　　　　void getChars(int sourceStart,int sourceEnd,char target[],int targetStart)

　　(6)、append() 可把任何类型数据的字符串表示连接到调用的StringBuffer对象的末尾。
　　　　例：int a=42;
　　　　　　StringBuffer sb=new StringBuffer(40);
　　　　　　String s=sb.append("a=").append(a).append("!").toString();

　　(7)、insert() 插入字符串
　　　　StringBuffer insert(int index,String str)
　　　　StringBuffer insert(int index,char ch)
　　　　StringBuffer insert(int index,Object obj)
　　　　index指定将字符串插入到StringBuffer对象中的位置的下标。

　　(8)、reverse() 颠倒StringBuffer对象中的字符
　　　　StringBuffer reverse()

　　(9)、delete()和deleteCharAt() 删除字符
　　　　StringBuffer delete(int startIndex,int endIndex)
　　　　StringBuffer deleteCharAt(int loc)

　　(10)、replace() 替换
　　　　StringBuffer replace(int startIndex,int endIndex,String str)

　　(11)、substring() 截取子串
　　　　String substring(int startIndex)
　　　　String substring(int startIndex,int endIndex)



