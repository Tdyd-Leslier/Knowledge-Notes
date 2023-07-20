# Markdown 学习笔记

Markdown 是一种轻量级标记语言，它允许人们使用易读易写的纯文本格式编写文档，然后转换成格式丰富的 HTML 页面。

## 1. 标题

要创建标题，请在文本前添加 # ，# 的数量代表了标题的级别。

    # Heading level 1

# Heading level 1

    ## Heading level 2

## Heading level 2

    ### Heading level 3

### Heading level 3

注意：不同的 Markdown 应用程序处理 # 和标题之间的空格（space）数量并不一致。考虑到兼容性问题，请用 1 个空格将 # 和标题进行分隔。

## 2. 段落

要创建段落，请用空白行将一行或多行文本进行分隔，不要用空格或制表符（tab）缩进段落。

Markdown 换行有 3 种方式。

- 在行尾添加两个或多个空格，然后输入回车键（return）。
- 在行尾添加 HTML 的 \<br> 标签。
- 无需在行尾添加任何内容，只需输入回车键。

注意：第 1 种方式是有争议的，因为很难在编辑器中直接看到空格，相比更推荐第 2 和第 3 种方式。此外，CommonMark 和其它几种轻量级标记语言支持在行尾添加 \\ 的方式实现换行，但并非所有 Markdown 应用程序都支持此方式，因此不推荐。

## 3. 列表

要创建有序列表，请在每个列表项前添加数字并紧跟 1 个英文句点，并添加 1 个空格。

    1. First item
    2. Second item
    3. Third item
    4. Fourth item

1. First item
2. Second item
3. Third item
4. Fourth item

要创建无序列表，请在每个列表项前面添加 - 、* 或 + ，并添加 1 个空格。

    - First item
    - Second item
    - Third item
    - Fourth item

- First item
- Second item
- Third item
- Fourth item

缩进一个或多个列表项可创建嵌套列表。

    - First item
    - Second item
    - Third item
      - Indented item
        - Indented item
    - Fourth item

- First item
- Second item
- Third item
  - Indented item
    - Indented item
- Fourth item

要在保留列表连续性的同时在列表中添加另一种元素，请将该元素缩进 4 个空格或 1 个制表符。

    - This is the first list item.
    - Here's the second list item.

      I need to add another paragraph below the second list item.

    - And here's the third list item.

- This is the first list item.
- Here's the second list item.
  
  I need to add another paragraph below the second list item.

- And here's the third list item.

代码块通常采用 4 个空格或 1 个制表符缩进。当它们被放在列表中时，请将它们缩进 8 个空格或 2 个制表符。

    1. Open the file.
    2. Find the following code block on line 21:
 
           <html>
             <head>
               <title>Test</title>
             </head>
           <html>

    3. Update the title to match the name of your website.

1. Open the file.
2. Find the following code block on line 21:

       <html>
         <head>
           <title>Test</title>
         </head>
       <html>

3. Update the title to match the name of your website.

一些 Markdown 应用程序允许创建定义列表，github 貌似不可以。要创建定义列表，请在第一行输入术语。在下一行输入 : 并添加 1 个空格。

      First Term
      : This is the definition of the first term.

      Second Term
      : This is one definition of the second term.
      : This is another definition of the second term.

First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.

## 4. 表格

要创建表格，请用三个或多个 --- 创建每列的标题，并用 | 分隔每列。

    | 表头  | 表头  |
    |-----|-----|
    | 单元格 | 单元格 |
    | 单元格 | 单元格 |

| 表头  | 表头  |
|-----|-----|
| 单元格 | 单元格 |
| 单元格 | 单元格 |

要对齐，请用 :- 设置内容和标题栏居左对齐，:-: 设置内容和标题栏居中对齐，-: 设置内容和标题栏居右对齐。

    | 居左对齐 | 居右对齐 | 居中对齐 |
    |:-----|-----:|:-----:|
    | 单元格 | 单元格 | 单元格  |
    | 单元格 | 单元格 | 单元格  |

| 居左对齐 | 居右对齐 | 居中对齐 |
|:-----|-----:|:-----:|
| 单元格 | 单元格 | 单元格  |
| 单元格 | 单元格 | 单元格  |

注意：可以在表格中设置文本格式，但不能添加标题，区块，列表，图像或 HTML 标签等。

可借助使用在线表格编辑工具 [Markdown Table](https://tableconvert.com/markdown-to-markdown)

## 5. 图片

要插入图片，请用基础格式：\!\[图片关键词](图片链接 "图片 title") 编写插入 3 种不同类型的图片。

- 本地图片：在基础格式的括号中输入图片的位置路径即可，支持绝对路径和相对路径。
- 网络图片：在基础格式的括号中输入图片的网络链接即可，可选用免费或收费图床，但缺点是将图片存在网络服务器上，非常依赖网络。
- Base64转码图片：可借助使用在线转码工具 [Base64](https://toolgg.com/image-to-base64.html) 把图片转成一段字符串，然后把字符串填入图片链接即可，但字符串一般很长，因此推荐和引用链接一起使用。

![Markdown 学习笔记](https://tdydleslier-picgo.oss-cn-guangzhou.aliyuncs.com/Markdown学习笔记/Markdown学习笔记.jpg)

## 6. 公式

    要数学表达式在行内显示，请用$math$
$y=x^2$

    要数学表达式在块内显示，请用$$math$$
$$y=x^2$$

可借助使用在线公式编辑工具 [Markdown Math](https://www.latexlive.com/)

## 7. 字体

    **粗体**

**粗体**

    *斜体*

*斜体*

    ***粗斜体***

***粗斜体***

    文本高亮：==文本高亮== ，github貌似不可以

==文本高亮==

    文本上标：x^2^，github貌似不可以

x^2^

    文本下标：H~2~O，github貌似不可以

H~2~O

## 8. 线

    分割线：***
***

    删除线：~~test~~

~~test~~

    下划线：<u>test</u>

<u>test</u>

## 9. 区块

要创建区块，请在段落前添加一个 > 符号。

    > Dorothy followed her through many of the beautiful rooms in her castle.

> Dorothy followed her through many of the beautiful rooms in her castle.

区块可以包含多个段落，请在段落之间的空白行添加一个 > 符号。

    > Dorothy followed her through many of the beautiful rooms in her castle.
    >
    > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

区块可以嵌套，请在要嵌套的段落前添加一个 >> 符号。

    > Dorothy followed her through many of the beautiful rooms in her castle.
    >
    >> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

区块可以包含其他 Markdown 格式的元素，但并非所有元素都可以使用。

    > ### The quarterly results look great
    >
    > - Revenue was off the chart.
    > - Profits were higher than ever.
    >
    > *Everything* is going according to **plan**.

> ### The quarterly results look great
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
> *Everything* is going according to **plan**.

## 10. 代码

要将文本表示为代码，请将其包裹在 ` 中。

    At the command prompt, type `nano`.

At the command prompt, type `nano`.

如果要表示为代码的文本中包含一个或多个 ` ，则请将文本包裹在 `` 中。

    ``Use `code` in your Markdown file.``

``Use `code` in your Markdown file.``

要创建代码块，请将代码块的每一行缩进至少 4 个空格或 1 个制表符。

    <html>
      <head>
        <title>Test</title>
      </head>
    <html>

也可以在代码块之前和之后的行上使用 \`\`\` 或 ~~~ ，并且可以在代码块之前 \`\`\` 后增加使用的语言。

    ```json
    {
    "firstName": "John",
    "lastName": "Smith",
    "age": 25
    }
    ```

```json
{
"firstName": "John",
"lastName": "Smith",
"age": 25
}
```

## 11. 链接

Markdown 中有 2 种方式实现链接，分别为内联链接和引用链接。

- 内联链接

要创建超链接，请使用： \[超链接显示名](超链接地址 "超链接title")。

[Markdown 学习笔记](https://github.com/Tdyd-Leslier/Knowledge-Notes/blob/main/Markdown-Notes/Markdown-Notes.md "最好的 Markdown 学习笔记")

还可以引用文档本身各标题。

[Markdown 学习笔记](#markdown-学习笔记 )

要将 URL 或者 Email 地址变成可点击的链接，请将其包裹在 <> 中。

<https://github.com/Tdyd-Leslier/Knowledge-Notes/blob/main/Markdown-Notes/Markdown-Notes.md>

要强调链接, 请在链接文本前后增加 * 。 要将链接表示为代码，请在方括号中添加 ` 。

I love supporting the **[Markdown-Notes](https://github.com/Tdyd-Leslier/Knowledge-Notes/blob/main/Markdown-Notes/Markdown-Notes.md)**.

This is the *[Markdown-Notes](https://github.com/Tdyd-Leslier/Knowledge-Notes/blob/main/Markdown-Notes/Markdown-Notes.md)*.

See the section on [`Markdown-Notes`](https://github.com/Tdyd-Leslier/Knowledge-Notes/blob/main/Markdown-Notes/Markdown-Notes.md).

- 引用链接

引用链接分为两部分，与文本保持内联的部分以及存储在文件中其他位置的部分，增加 Markdown 源文件的可读性。

      I get 10 times more traffic from [Google] [1] than from Yahoo or MSN.

      [1]: http://google.com/"Google"

I get 10 times more traffic from [Google] [1] than from Yahoo or MSN.

[1]: http://google.com/"Google"

注意：许多 Markdown 应用程序会自动将 URL 转换为链接，这意味着如果输入 `http://google.com` ，即使未使用 <> ，也会自动将其转换为链接。如果不希望自动链接 URL ，则可以将其包裹在 `` 中。

## 12. 高级技巧

- 快捷键

      Ctrl+K Z：专注模式
      Ctrl+B：粗体
      Ctrl+I：斜体
      Ctrl+/：注释

- 转义字符

要显示原本用于格式化 Markdown 文档的字符，请在字符前面添加 \ 。

- 表情符号

一些 Markdown 应用程序允许通过输入表情符号代码来插入表情符号，这些以冒号开头和结尾，并包含表情符号的名称。

具体可参考 [Markdown Emotion](https://gist.github.com/rxaviers/7360908)

- 任务列表

任务列表使可以创建带有复选框的项目列表。在支持任务列表的 Markdown 应用程序中，复选框将显示在内容旁边。要创建任务列表，请在任务列表项之前添加 - 和 [] ，并在 [] 前面加上空格。要选择一个复选框，请在 [] 之间添加 x 。

- [x] Write the press release
- [x] Update the website
- [ ] Contact the media

## 更多 Markdown 语法请查阅 [Markdown官方教程](https://markdown.com.cn/)
