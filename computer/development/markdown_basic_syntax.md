## [Markdown 基础语法](./markdown_basic_syntax)

##### *Made by* [AImator.com]()

本节主要介绍了 Markdown 的基础语法，仅针对较难理解的部分附上效果展示加以说明。

### 本节纲要

- **[分级标题](#分级标题)**
- **[特殊标识](#特殊标识)**
	- [粗体](#粗体)
	- [斜体](#斜体)
	- [代码](#代码)
	- [删除线](#删除线)
- **[引用](#引用)**
	- [一般引用](#一般引用)
	- [分级引用](#分级引用)
- **[清单](#清单)**
	- [无序清单](#无序清单)
	- [有序清单](#有序清单)
- **[添加链接](#添加链接)**
	- [文字链接](#文字链接)
	- [图片链接](#图片链接)
- **[反斜杠转义符](#反斜杠转义符)**

---

### [分级标题](#分级标题)

```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

### [特殊标识](特殊标识)

#### [粗体](#粗体)

```
**粗体**
```

#### [斜体](#斜体)

```
*斜体*
```

#### [代码](#代码)

```
`代码`
```

#### [删除线](#删除线)

```
~~删除线~~
```

### [引用](#引用)

引用分为一般引用和分级引用。

#### [一般引用](#一般引用)

```
> 知识就是力量
```

#### [分级引用](#分级引用)

```
> 开发技术包括
> > 前端开发和后端开发等，前端开发又可以细分为
> > > 网页开发和应用开发等诸多领域。
```

### [清单](#清单)

清单分为无序清单和有序清单。

#### [无序清单](#无序清单)

```
* 项目 1
* 项目 2
	* 项目 2a
	* 项目 2b
```

#### [有序清单](#有序清单)

```
1. 项目 1
1. 项目 2
1. 项目 3
	1. 项目 3a
	1. 项目 3b
```

### [添加链接](#添加链接)

#### [文字链接](#文字链接)

```
[文字部分](链接部分)
```

#### [图片链接](#图片链接)

```
![图片名称](图片链接)
```

### [反斜杠转义符](#反斜杠转义符)

日常文本写作过程中，具有标记作用的语法符号，通常无法直接显示出来，当我们需要将其作为普通符号出现在文本中时，需要用到反斜杠转义符 `\` 使其失去标记语法的作用。

```
\*markdown\*
\*\*markdown\*\*
```

上述代码将显示如下效果:

\*markdown\*

\*\*markdown\*\*

反斜杠转义符适用于以下具有标记作用的语法符号:

```
 \   backslash
 `   backtick
 *   asterisk
 _   underscore
{ }  curly braces
[ ]  square brackets
( )  parentheses
 #   hash mark
 +   plus sign
 -   minus sign (hyphen)
 .   dot
 !   exclamation mark
```

#### [返回本节纲要](#本节纲要)
#### [返回本章大纲](./markdown)
