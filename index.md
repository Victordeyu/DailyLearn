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

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Victordeyu/DailyLearn/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
