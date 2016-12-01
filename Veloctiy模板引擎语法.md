# 注释

##### 单行注释

```
## 注释内容
```

##### 多行注释

```
\#*
  注释内容
  注释内容
*#
```

##### 文档注释

```
\#**
  @version
  @author
*#
```

# references （引用）的几种格式

##### 变量

```
${a}
$a
$msg
```

##### 属性

```
${a.foo}
```

##### 方法

```
${a.fun()}
$TagUtil.options()
```

```
  "{}"用来明确标识Velocity对象，如在页面中有一个$someonename，此时变量
  名为someonename。但是若想someone这个变量后紧接着显示name字符，则改
  为${someone}name
```

#### "!"强制把不存在的变量或者还没值的变量输出为空白

```
  当页面中包含$a时，若a变量有值，则输出a的值，如果变量a没值，则显示字
  符$a。为了将不存在的变量，或者变量值为null的对象显示为空白，用 `$!a`
```

# #号标识

  ‘#’用来标识Velocity的脚本语句，包括#set，#if，#else，#end，#foreach，#iinclude，#parse，#macro等

```
#if($info.imgs)
<img src="$info.imgs" border=0 />
#else
<img src="noPhoto.jpg" />
#end
```

# directives（指令）

## #set定义/设置变量

##### 字符串

```
#set($a = "Velocity")
```

##### 数值

```
#set($a = 123456)
```

##### 数组

```
#set($a.arr = ["Not", $foo, "fault"])
```

##### 变量

```
#set($a = $b)
```

##### 属性

```
#set($a.attr = $b.attr)
```

##### 方法

```
#set($a.Plan = $b.fun($web))
```

##### 算术表达式

```
#set($a = $b + 1)
```
