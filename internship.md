### 实习相关

接单页
预定城市 搜索线路 内容匹配值修改 后端返回值要求 洲--国家--一级区域--二级区域--行政区--街道/镇--商业区 格式 
后端调用服务不同 与产品、后端一起开会研讨
后端改接口 换请求 调整相应入参和返回数据结构 搜索逻辑做出相应改变 


host: C:\Windows\System32\drivers\etc\hosts   
驼峰命名 健壮性   
+ 下拉框数组去重   
关联取票人姓名下拉框，联系人+出游人的并集，但是要去重
[参考](https://segmentfault.com/a/1190000003984330)

+ 图片img的src不变让浏览器重新加载实现方法        
图片img的src不变,想让浏览器重新加载怎么办,在图片地址src不变的情况下让浏览器重新加载图片,实际上在src不变时，浏览器直接就去读取缓存   
javascript给这个img标签的src属性后面拼接一个 ? 和 javascript对象new Date().getTime()毫秒值做成queryString的样子，就能防止被缓存了   
在图片地址src不变的情况下让浏览器重新加载图片    
实际上，在src不变时，浏览器直接就去读取缓存了     
解决办法： 
var img_src ='http://www.ilsea.net/images/seagull.jpg?t='+Math.random(); 
这样给图片地址拼接一个随机数，用js重新给 img 的 src 赋值，okay 

+  vue2.0中mounted后不能保证到有vue实例了
   在mounted加个this.$nextTick方法   
   将回调延迟到下次 DOM 更新循环之后执行。在修改数据之后立即使用它，然后等待 DOM 更新。它跟全局方法 Vue.nextTick 一样，不同的是回调的 this 自动绑定到    调用它的实例上。
   
+ Number()、parseInt()、parseFloat()的区别  
1. Number():可以用于任何数据类型转换成数值；
parseInt()、parseFloat():专门用于把字符串转换成数值；
2. Number()  
Number():   
```
1）如果是Boolean值，true和false将分别转换为1和0。

2）如果是数字值，只是简单的传入和返回。

3）如果是null值，返回0。

4）如果是undefined,返回NaN。

5）如果是字符串，遵循下列规则：
```

```
如果是字符串中只包含数字（包括前面带正号或负号的情况），则将其转换为十进制数值，即“1”变成1，“123”会变成123，而“011”会变成11（前导的零被忽略了）；
如果字符串中包含有效的浮点格式，如“1.1”，则将其转换为对应的浮点数值（同样也会忽略前导零）；
如果字符串中包含有效的十六进制格式，例如"0xf"，则将其他转换为相同大小的十进制整数值；
如果字符串是空的（不包含任何字符），则将其转换为0；
如果字符串中包含除上述格式之外的字符，则将其他转换成NaN.
6)如果是对象，则调用对象的valueOf()方法，然后依照前面的规则转换返回的值。如果转换的结果是NaN，则调用的对象的toString()方法，然后再次依照前面的规则转换返回的字符串值。

ex:

var num1=Number("Hello World");  //NaN

var num2=Number("");                  //0

var num3=Number("000011");      //11

var num4=Number(true);             //1
```
3. 由于Number()函数在转换字符串时比较复杂而且不够合理，因此在处理整数的时候更常用的是parseInt()函数。

parseInt():
```
在转换字符串时，更多的时看其是否符合数值模式。会忽略字符串前面的空格，直至找到第一个非空格字符。

如果第一个字符不是数字字符或都负号，parseInt()就会返回NaN; 也就是说，用parseInt()转换空字符串会返回NaN。
如果第一个字符是数字字符，parseInt()会继续解析第二个字符，直到解析完所有后续字符或者遇到了一个非数字字符。例如，"1234blue"会被转换为1234，因为"blue"会被完全忽略。类似地"22.5"会被转换为22，因为小数点不是有效的数字字符。
如果字符串以"0x"开头且后跟数字字符，就会将其当作一个十六进制整数；
如果字符串以"0"开头且后跟数字字符，就会将其当作一个八进制整数；
parseInt()函数增加了第二参数用于指定转换时使用的基数（即多少进制）如：parseInt("10",16)//按十六进制解析；parseInt("10",8)//按八进制解析
parseFloat():
```
parseInt()
```
与parseInt()函数类似，C也是从第一个字符（位置0）形如解析每个字符，而且也是一直解析到字符串末尾，或者解析到遇见一个无效的浮点数字字符为止。也就是说，字符串中的第一个小数点是有效的，而第二个小数点就是无效的了，因此它后面的字符串将被忽略。例如："22.34.5"将会转换为22.34。

除了第一个小数点有效之外，parseFloat()与parseInt()的第二个区别在于它始终都会忽略前导的零。parseFloat()可以识别前面讨论过的所有的浮点数值格式，也包括十进制整数格式。但十六进制格式的字符串则始终会被转换成0。由于parseFloat()只解析十进制值，因此它没有用第二个参数指定基数的用法。

另外，如果字符串包含的是一个可解析为整数的数（没有小数点，或者小数点后面都是零），parseFloat()会返回整数。

ex: 

var num1=parseFloat("1234blue");  //1234

var num2=parseFloat("0xA");                  //0

var num3=parseFloat("0908.5");      //908.5

var num4=parseFloat("3.125e7");             //31250000
```


商旅部分 

slidebar 组件  art-template
css 预订人与邮箱样式调整 机票下单信息提示优化
商旅出游表单内容改变 逻辑调整 入住人数 格式校验等


团队游
Boss3订单系统
根据需求文档
修改订单详情
与后端交流 门票资源 某接口返回值 outorderID  buyNum等 返回错误 预期为1 ,导致前端显示错误 

ftl的修改 

行程订制系统 vue  
侧边栏行程报价逻辑
点击获取按钮的gtype显示跳转到不同页面

gulp 打包 gulp build_dev   改完js编译

比如 ： 促销、旅游券、抵用券使用情况：

若订单中未参加促销活动、未使用旅游券和抵用券，则直接为空，客服可以手动编辑，限制300字；

若订单中参加了促销活动，则默认带入：促销活动名称 优惠n元

若订单中使用了抵用券，则默认带入：使用抵用券 优惠n元

若订单中使用了旅游券，则默认带入：使用旅游券 n元

若订单中选择了保险，则默认带入：【保险类型】保险名称 份数

客服均可以编辑。
代码提交的过程为：branch ——>  test_diy   ——>  test  ——>   stable.
