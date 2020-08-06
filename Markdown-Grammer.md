<span id="top"></span>
## 1.标题
# 这是一级标题
## 这是二级标题
### 这是三级标题
#### 这是四级标题
##### 这是五级标题
###### 这是六级标题
## 2.字体
**这是加粗的文字**  
*这是倾斜的文字*  
***这是斜体加粗的文字***  
~~这是加删除线的文字~~
## 3.引用
>引用的内容1
>>引用的内容2  
换个行试试
>>>引用的内容3
## 4.分割线(-和*)  
---
***
## 5.图片
![替代文字](https://avatars0.githubusercontent.com/u/37428346?s=96&v=4 "提示信息")
## 6.超链接
[百度一下(markdown)](http://baidu.com "百度Hint")  
<a href="http://baidu.com" target="_blank">百度一下(html格式)</a>

[百度一下(脚注)][1]
<www.baidu.com>
## 7.列表
### 无序列表(-或=或*)
- 项目1
+ 项目2
* 项目3
### 有序列表（数字+.）
1. 项目1
2. 项目2
3. 项目3
### 嵌套列表
* 项目1 
  * 项目1.1(只需要一个tab哦)
  * 项目1.2
    * 项目1.2.1
    * 项目1.2.2
* 项目2
1. 项目1 
    1. 项目1.1(需要两个tab哦)
    2. 项目1.2
        1. 项目1.2.1
        1. 项目1.2.2
2. 项目2
## 8.表格
<!--第二行是为了把内容和表头分开-->
姓名|技能|排行
--|:--:|--:
刘备|哭|大哥
关羽|打|二哥
张飞|骂|三弟
## 9.代码
<!--单行代码-->
`create database hero;`
<!--代码块-->
```
int add(int x, int y){
     return x + y;
}
fun();
```
## 10.流程图（github不支持）
```flow
st=>start: 开始
op=>operation: My Operation
cond=>condition: Yes or No?
e=>end
st->op->cond
cond(yes)->e
cond(no)->op
```
[1]:http://www.baidu.com "百度"
[top](#top)
