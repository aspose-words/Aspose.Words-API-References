---
title: range property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns a [Range](../../range/) object that represents the portion of a document that is contained in this node."
type: docs
weight: 80
url: /python-net/aspose.words/node/range/
---

## Node.range property

Returns a [Range](../../range/) object that represents the portion of a document that is contained in this node.



### Examples

Shows how to delete all the nodes from a range.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add text to the first section in the document, and then add another section.
builder.write("Section 1. ")
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.write("Section 2.")

self.assertEqual("Section 1. \fSection 2.", doc.get_text().strip())

# Remove the first section entirely by removing all the nodes
# within its range, including the section itself.
doc.sections[0].range.delete()

self.assertEqual(1, doc.sections.count)
self.assertEqual("Section 2.", doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

