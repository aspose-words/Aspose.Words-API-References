---
title: CompositeNode.last_child property
linktitle: last_child property
articleTitle: last_child property
second_title: Aspose.Words for Python
description: "CompositeNode.last_child property. Gets the last child of the node."
type: docs
weight: 50
url: /ru/python-net/aspose.words/compositenode/last_child/
---

## CompositeNode.last_child property

Gets the last child of the node.


```python
@property
def last_child(self) -> aspose.words.Node:
    ...

```

### Remarks

If there is no last child node, a ``None`` is returned.



### Examples

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Section 1 text.')
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.writeln('Section 2 text.')
# Оба раздела являются соседями друг для друга.
last_section = doc.last_child.as_section()
first_section = last_section.previous_sibling.as_section()
# Удалите раздел, основываясь на его отношениях соседства с другим разделом.
if last_section.previous_sibling != None:
    doc.remove_child(first_section)
# Раздел, который мы удалили, был первым, оставив документ только со вторым.
self.assertEqual('Section 2 text.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

