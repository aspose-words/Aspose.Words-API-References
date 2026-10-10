---
title: Node.previous_sibling property
linktitle: previous_sibling property
articleTitle: previous_sibling property
second_title: Aspose.Words for Python
description: "Node.previous_sibling property. Gets the node immediately preceding this node."
type: docs
weight: 70
url: /sv/python-net/aspose.words/node/previous_sibling/
---

## Node.previous_sibling property

Gets the node immediately preceding this node.


```python
@property
def previous_sibling(self) -> aspose.words.Node:
    ...

```

### Remarks

If there is no preceding node, a ``None`` is returned.



### Examples

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Section 1 text.')
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.writeln('Section 2 text.')
# Båda sektionerna är syskon till varandra.
last_section = doc.last_child.as_section()
first_section = last_section.previous_sibling.as_section()
# Ta bort en sektion baserat på dess syskonrelation med en annan sektion.
if last_section.previous_sibling != None:
    doc.remove_child(first_section)
# Sektionen vi tog bort var den första, vilket lämnar dokumentet med endast den andra.
self.assertEqual('Section 2 text.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

