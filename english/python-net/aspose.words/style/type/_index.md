---
title: Style.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "Style.type property. Gets the style type (paragraph or character)."
type: docs
weight: 180
url: /python-net/aspose.words/style/type/
---

## Style.type property

Gets the style type (paragraph or character).


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

