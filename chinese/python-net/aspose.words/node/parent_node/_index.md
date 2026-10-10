---
title: Node.parent_node property
linktitle: parent_node property
articleTitle: parent_node property
second_title: Aspose.Words for Python
description: "Node.parent_node property. Gets the immediate parent of this node."
type: docs
weight: 60
url: /zh/python-net/aspose.words/node/parent_node/
---

## Node.parent_node property

Gets the immediate parent of this node.


```python
@property
def parent_node(self) -> aspose.words.CompositeNode:
    ...

```

### Remarks

If a node has just been created and not yet added to the tree,
or if it has been removed from the tree, the parent is ``None``.




### Examples

Shows how to create a node and set its owning document.

```python
from api_example_base import ApiExampleBase
doc = aw.Document()
para = aw.Paragraph(doc)
para.append_child(aw.Run(doc=doc, text='Hello world!'))
# 我们尚未将此段落作为子节点追加到任何复合节点。
self.assertIsNone(para.parent_node)
# 如果一个节点是另一个复合节点的适当子节点类型，
# 只有当两个节点具有相同的所有者文档时，我们才能将其作为子节点附加。
# 所有者文档是我们在节点构造函数中传入的文档。
# 我们尚未将此段落附加到文档中，因此文档不包含其文本。
self.assertEqual(para.document, doc)
self.assertEqual('', doc.get_text().strip())
# 由于文档拥有此段落，我们可以将其样式之一应用于段落的内容。
para.paragraph_format.style = doc.styles.get_by_name('Heading 1')
# 将此节点添加到文档中，然后验证其内容。
doc.first_section.body.append_child(para)
self.assertEqual(doc.first_section.body, para.parent_node)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

