---
title: remove_child method
second_title: Aspose.Words for Python via .NET API Reference
description: "Removes the specified child node."
type: docs
weight: 160
url: /python-net/aspose.words/compositenode/remove_child/
---

## remove_child(old_child) {#node}

Removes the specified child node.


```python
def remove_child(self, old_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| old_child | [Node](../../node/) |  |

The parent of oldChild is set to null after the node is removed.




### Returns

The removed node.


### Examples

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Section 1 text.")
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.writeln("Section 2 text.")

# Both sections are siblings of each other.
last_section = doc.last_child.as_section()
first_section = last_section.previous_sibling.as_section()

# Remove a section based on its sibling relationship with another section.
if last_section.previous_sibling is not None:
    doc.remove_child(first_section)

# The section we removed was the first one, leaving the document with only the second.
self.assertEqual("Section 2 text.", doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

