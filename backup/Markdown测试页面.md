# Markdown 元素测试页面

这个页面展示了所有常见的 Markdown 元素及其语法。

> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.

## 1. 标题

# H1 标题
## H2 标题
### H3 标题
#### H4 标题
##### H5 标题
###### H6 标题

## 2. 文本样式

**粗体文本**
*斜体文本*
***粗斜体文本***
~~删除线文本~~
<u>下划线文本</u>
`行内代码`
H~2~O（下标）
X^2^（上标）

==高亮文本==

## 3. 列表

### 无序列表
- 项目一
- 项目二
  - 子项目一
  - 子项目二
    - 孙项目
- 项目三

### 有序列表
1. 第一项
2. 第二项
   1. 子项一
   2. 子项二
3. 第三项

### 任务列表
- [x] 已完成任务
- [ ] 待完成任务
- [ ] 另一个任务

## 4. 引用

> 这是一个引用
> 
> 引用中的第二段
> 
> > 嵌套引用
> 
> 回到第一层引用

## 5. 代码块

行内代码：`console.log("Hello World")`

### JavaScript 代码
```javascript
function helloWorld() {
    console.log("Hello, World!");
    return 42;
}
```

### Python 代码
```python
def hello_world():
    print("Hello, World!")
    return 42
```

### 纯文本代码
```
没有任何语法高亮的代码块
```

## 6. 表格

| 列1标题 | 列2标题 | 列3标题 |
|---------|---------|---------|
| 单元格1 | 单元格2 | 单元格3 |
| 左对齐 | 居中对齐 | 右对齐 |
| 数据1 | 数据2 | 数据3 |

### 对齐方式
| 左对齐 | 居中对齐 | 右对齐 |
|:--------|:--------:|--------:|
| 文本左 | 文本中 | 文本右 |
| 数据左 | 数据中 | 数据右 |

## 7. 链接和图片

[普通链接](https://example.com)
[带标题的链接](https://example.com "链接标题")

### 引用式链接
这是一个引用式链接：[示例][1]和另一个[引用][2]

[1]: https://example.com "示例链接"[2]: https://example.org

## 8. 分割线

下面是分割线：

---

另一种分割线：

***

## 9. 脚注

这是一个带有脚注的文本[^1]。

这是另一个脚注[^2]。

[^1]: 这是第一个脚注的内容。
[^2]: 这是第二个脚注的内容，可以包含多行文本。