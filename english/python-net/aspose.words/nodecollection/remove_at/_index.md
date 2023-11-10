---
title: NodeCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "NodeCollection.remove_at method. Removes the node at the specified index from the collection and from the document."
type: docs
weight: 90
url: /python-net/aspose.words/nodecollection/remove_at/
---

## remove_at(index) {#int}

Removes the node at the specified index from the collection and from the document.


```python
def remove_at(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |

### Examples

Shows how to add and remove sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Section 1")
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write("Section 2")

self.assertEqual("Section 1\u000cSection 2", doc.get_text().strip())

# Delete the first section from the document.
doc.sections.remove_at(0)

self.assertEqual("Section 2", doc.get_text().strip())

# Append a copy of what is now the first section to the end of the document.
last_section_idx = doc.sections.count - 1
new_section = doc.sections[last_section_idx].clone()
doc.sections.add(new_section)

self.assertEqual("Section 2\u000cSection 2", doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

