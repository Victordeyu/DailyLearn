## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/Victordeyu/DailyLearn/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

# KMP算法

## 如何获得next

### 对于一个0开头的next数组。next[0]=0 next[1]=1。

### 当j>1时,会根据next[j-1]来计算，具体如下：

  我们先把j向后移动一位，从而生成了新的字串，记为S_[j]。next[j]即为新字串P_[1]...P_[j-1]的前后缀最大匹配数（+1）。
首先next[j-1]会标识了j-1个元素前面可以匹配的最大长度的前缀s1，因此我们可以直接从该最大长度的前缀s1开始匹配。s1的下一位是next[j-1]。（0开始的next数组要比实际可以匹配的最大前缀大1，所以next[j-1]刚好标识了最大前缀的后一位元素）而与最大前缀相匹配的最大后缀的后一位是P_[j-1]。

  因此，我们可以判断P_next[j-1]==P_[j-1]。如果相同，说明新字串有一个更大的前后缀最大匹配数。所以next[j]=next[j-1]+1。
  当P_next[j-1]!=P_[j-1]时，说明新字串不会有更大的匹配数。从而我们要去找更小的匹配数。
  
  接下来，我们从一张图来看现在的匹配情况。如图是整个Pattern（待匹配字符串）的一部分。可以看到next[J-1]-1标识了红色部分的长度（即J-1元素的前后缀最大匹配数）。而next[J-1]则标识了可匹配的前缀后的第一个元素。
  
  ![Image](https://github.com/Victordeyu/DailyLearn/blob/gh-pages/KMP/getNext.png)
  
  我们记P_next[J-1]为元素n。P_next[j-1]!=P_[j-1]意味着红色部分无法被延长，只能被缩短。如果从P_[next[J-1]-1]开始匹配会浪费大量时间。此时我们会发现，next[N]-1已经标记了元素N在前面的红色子串中可匹配的最大前后缀的长度。而next[N]正是它在红色字串中无法匹配的第一个前缀，记为M。此时，我们可以直接用M来与P[J-1]来匹配。因为两端红色的字串是完全一样的，这意味着在P[J-1]前也有一段完全一样的相同字串。我们以此循环往复来搜寻整个红色字串中与它匹配的最大前缀。

  以此来看，所有的next值都可以以这样的方式递归得到。这个过程中，我们把j来不断地赋值成next[j]。当next[j]==0时，说明我们已经搜索到了红色字串的左端边界。这样说明没有字串可以与它匹配，因此赋值为1。


### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](https://github.com/Victordeyu/DailyLearn/blob/gh-pages/KMP/getNext.png)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Victordeyu/DailyLearn/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
