---
title: Font.all_caps property
linktitle: all_caps property
articleTitle: all_caps property
second_title: Aspose.Words for Python
description: "Font.all_caps property. True if the font is formatted as all capital letters."
type: docs
weight: 10
url: /zh/python-net/aspose.words/font/all_caps/
---

## Font.all_caps property

True if the font is formatted as all capital letters.


```python
@property
def all_caps(self) -> bool:
    ...

@all_caps.setter
def all_caps(self, value: bool):
    ...

```

### Examples

Shows how to format a run to display its contents in capitals.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# 有两种方法可以让运行在不更改内容的情况下将小写文本显示为大写。
# 1 - 将 AllCaps 标志设置为以常规大写字母显示所有字符：
run = aw.Run(doc=doc, text='all capitals')
run.font.all_caps = True
para.append_child(run)
para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()
# 2 - 将 SmallCaps 标志设置为以小型大写字母显示所有字符：
# 如果字符是小写，它将以大写形式出现
# 但高度与小写相同（字体的 x-height）。
# 原本为大写的字符将保持不变。
run = aw.Run(doc=doc, text='Small Capitals')
run.font.small_caps = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.Caps.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

