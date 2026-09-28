---
title: CompositeNode.remove_child method
linktitle: remove_child method
articleTitle: remove_child method
second_title: Aspose.Words for Python
description: "CompositeNode.remove_child method. Removes the specified child node."
type: docs
weight: 170
url: /zh/python-net/aspose.words/compositenode/remove_child/
---

## remove_child(old_child) {#node}

Removes the specified child node.


```python
def remove_child(self, old_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| old_child | [Node](../../node/) | The node to remove. |

### Remarks

The parent of *oldChild* is set to``None`` after the node is removed.




### Returns

The removed node.


### Examples

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Section 1 text.')
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.writeln('Section 2 text.')
# 两个节彼此是兄弟节点。
last_section = doc.last_child.as_section()
first_section = last_section.previous_sibling.as_section()
# 根据节与另一个节的兄弟关系移除该节。
if last_section.previous_sibling != None:
    doc.remove_child(first_section)
# 我们移除的节是第一个，导致文档仅剩下第二个节。
self.assertEqual('Section 2 text.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

