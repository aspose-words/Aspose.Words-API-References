---
title: clone method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.Document.clone method"
type: docs
weight: 550
url: /python-net/aspose.words/document/clone/
---

## clone() {#default}

Performs a deep copy of the [Document](../).



```python
def clone(self):
    ...
```

### Returns

The cloned document.


## clone(is_clone_children) {#bool}

Performs a deep copy of the [Document](../).



```python
def clone(self, is_clone_children: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| is_clone_children | bool |  |

### Returns

The cloned document.


## Examples

Shows how to deep clone a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Hello world!")

# Cloning will produce a new document with the same contents as the original,
# but with a unique copy of each of the original document's nodes.
clone = doc.clone()

self.assertEqual(doc.first_section.body.first_paragraph.runs[0].get_text(), clone.first_section.body.first_paragraph.runs[0].text)
self.assertIsNot(doc.first_section.body.first_paragraph.runs[0], clone.first_section.body.first_paragraph.runs[0])
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

