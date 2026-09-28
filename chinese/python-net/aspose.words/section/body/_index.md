---
title: Section.body property
linktitle: body property
articleTitle: body property
second_title: Aspose.Words for Python
description: "Section.body property. Returns the [Body](../../body/) child node of the section."
type: docs
weight: 20
url: /zh/python-net/aspose.words/section/body/
---

## Section.body property

Returns the [Body](../../body/) child node of the section.



```python
@property
def body(self) -> aspose.words.Body:
    ...

```

### Remarks

[Body](../../body/) contains main text of the section.

Returns ``None`` if the section does not have a [Body](../../body/) node among its children.




### Examples

Clears main text from all sections from the document leaving the sections themselves.

```python
doc = aw.Document()
# 空白文档包含一个节、一个正文和一个段落。
# 调用 "RemoveAllChildren" 方法以移除所有这些节点，
# 并得到一个没有子节点的文档节点。
doc.remove_all_children()
# 此文档现在没有可添加内容的复合子节点。
# 如果我们想编辑它，需要重新填充其节点集合。
# 首先，创建一个新节，然后将其作为子节点追加到根文档节点。
section = aw.Section(doc)
doc.append_child(section)
# 节需要一个正文，用于包含并显示其所有内容
# 在页面上位于节的页眉和页脚之间。
body = aw.Body(doc)
section.append_child(body)
# 此正文没有子元素，因此我们暂时无法向其添加运行。
self.assertEqual(0, doc.first_section.body.get_child_nodes(aw.NodeType.ANY, True).count)
# 调用 "EnsureMinimum" 以确保此正文至少包含一个空段落。
body.ensure_minimum()
# 现在，我们可以向正文添加运行，并让文档显示它们。
body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

