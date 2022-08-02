---
title: to_array method
second_title: Aspose.Words for Python via .NET API Reference
description: "Copies all paragraphs from the collection to a new array of paragraphs."
type: docs
weight: 20
url: /python-net/aspose.words/paragraphcollection/to_array/
---

## to_array() {#default}

Copies all paragraphs from the collection to a new array of paragraphs.


```python
def to_array(self):
    ...
```

### Returns

An array of paragraphs.


### Examples

Shows how to create an array from a NodeCollection.

```python
doc = aw.Document(MY_DIR + "Paragraphs.docx")

paras = doc.first_section.body.paragraphs.to_array()

self.assertEqual(22, len(paras))
```

Shows how to use "hot remove" to remove a node during enumeration.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("The first paragraph")
builder.writeln("The second paragraph")
builder.writeln("The third paragraph")
builder.writeln("The fourth paragraph")

# Remove a node from the collection in the middle of an enumeration.
for para in doc.first_section.body.paragraphs:
    para = para.as_paragraph()
    if "third" in para.range.text:
        para.remove()

self.assertNotIn("The third paragraph", doc.get_text())
```

### See Also

* module [aspose.words](../../)
* class [ParagraphCollection](../)

