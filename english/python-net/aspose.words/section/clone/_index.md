---
title: clone method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.Section.clone method"
type: docs
weight: 110
url: /python-net/aspose.words/section/clone/
---

## clone() {#default}

Creates a duplicate of this section.


```python
def clone(self):
    ...
```

## clone(is_clone_children) {#bool}

Creates a duplicate of this section.


```python
def clone(self, is_clone_children: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| is_clone_children | bool |  |

## Examples

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

## See Also

* module [aspose.words](../../)
* class [Section](../)

