## [Markdown 扩展语法](./markdown_extended_usage)

##### *Made by* [AImator.com]()

本章主要介绍了 markdown 基于 [Github](https://www.github.com) 平台使用的扩展语法。

### 语法高亮

在语法高亮
Here’s an example of how you can use syntax highlighting with [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown):

\`\`\`ruby
```
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
\`\`\`

You can also simply indent your code by four spaces:

```
    function fancyAlert(arg) {
      if(arg) {
        $.facebox({div:'#foo'})
      }
    }
```

Here’s an example of Python code without syntax highlighting:

```
def foo():
    if not bar:
        return True
```

### Task Lists

```
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
```

### Tables
You can create tables by assembling a list of words and dividing them with hyphens `-` (for the first row), and then separating each column with a pipe `|`:

```
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
```
Would become:

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
