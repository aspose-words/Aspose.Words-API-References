---
title: Story.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Story.last_paragraph property. Gets the last paragraph in the story."
type: docs
weight: 20
url: /zh/python-net/aspose.words/story/last_paragraph/
---

## Story.last_paragraph property

Gets the last paragraph in the story.


```python
@property
def last_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# 文档构建器有一个光标，它充当文档的部分
# 当我们使用其文档构建方法时，构建器在此处追加新节点。
# 此光标的功能与 Microsoft Word 的闪烁光标相同，
# 并且它总是位于构建器刚插入的任何节点之后紧接位置。
# 要将内容追加到文档的其他部分，
# 我们可以使用 "MoveTo" 方法将光标移动到另一个节点。
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# 光标现在位于我们移动到的节点前面。
# 添加第二个运行将把它插入到第一个运行之前。
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# 将光标移动到文档末尾，以继续像以前一样在末尾追加文本。
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

