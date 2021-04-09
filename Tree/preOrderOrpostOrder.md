## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/Victordeyu/DailyLearn/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

# 二叉树的遍历

### PreOrder and PostOrder

####  N L R
####  L R N

  可以看出前序和后序的区别在于叶子结点群与根结点群位置关系的不同。具体地说，如果某两个结点的关系为父子（祖先与子孙），那么他们在前序和后序遍历序列中的先后顺序必定是相反的。在前序遍历序列中靠前的结点是另一个结点的祖先（或父母结点）。
  
  推论：如果两个结点群在前序与后序序列中的相对位置保持不变，那么他们必定有同一个祖先。
       如果一个二叉树的前序与后序序列完全相反，那么没有一个结点有兄弟结点。（即所有结点都有祖孙关系）。

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

