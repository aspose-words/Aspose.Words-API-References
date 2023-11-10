---
title: Style.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Python
description: "Style.document property. Gets the owner document."
type: docs
weight: 50
url: /python-net/aspose.words/style/document/
---

## Style.document property

Gets the owner document.


```python
@property
def document(self) -> aspose.words.DocumentBase:
    ...

```

### Examples

Shows how to access a document's style collection.

```python
doc = aw.Document()

self.assertEqual(4, doc.styles.count)

# Enumerate and list all the styles that a document created using Aspose.Words contains by default.
for cur_style in doc.styles:
    print(f"Style name:\t\"{cur_style.name}\", of type \"{cur_style.type}\"")
    print(f"\tSubsequent style:\t{cur_style.next_paragraph_style_name}")
    print(f"\tIs heading:\t\t\t{cur_style.is_heading}")
    print(f"\tIs QuickStyle:\t\t{cur_style.is_quick_style}")

    self.assertEqual(doc, cur_style.document)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

