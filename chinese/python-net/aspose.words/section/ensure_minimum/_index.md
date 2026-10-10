---
title: Section.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Section.ensure_minimum method. Ensures that the section has [Section.body](../body/) with one [Paragraph](../../paragraph/)."
type: docs
weight: 130
url: /zh/python-net/aspose.words/section/ensure_minimum/
---

## ensure_minimum() {#default}

Ensures that the section has [Section.body](../body/) with one [Paragraph](../../paragraph/).



```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to prepare a new section node for editing.

```python
doc = aw.Document()
# 空白文档自带一个章节，该章节包含一个正文，正文中又有一个段落。
# 我们可以通过向该段落添加文本运行、形状或表格等元素来向此文档添加内容。
self.assertEqual(aw.NodeType.SECTION, doc.get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.BODY, doc.sections[0].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[0].body.get_child(aw.NodeType.ANY, 0, True).node_type)
# 如果我们这样添加一个新章节，它将没有正文，也没有其他子节点。
doc.sections.add(aw.Section(doc))
self.assertEqual(0, doc.sections[1].get_child_nodes(aw.NodeType.ANY, True).count)
# 运行 "EnsureMinimum" 方法，为此章节添加正文和段落，以开始编辑它。
doc.last_section.ensure_minimum()
self.assertEqual(aw.NodeType.BODY, doc.sections[1].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[1].body.get_child(aw.NodeType.ANY, 0, True).node_type)
doc.sections[0].body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

