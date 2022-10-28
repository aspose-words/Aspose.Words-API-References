---
title: previous_sibling property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the node immediately preceding this node."
type: docs
weight: 70
url: /python-net/aspose.words/node/previous_sibling/
---

## Node.previous_sibling property

Gets the node immediately preceding this node.

If there is no preceding node, a ``None`` is returned.



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
* class [Node](../)

