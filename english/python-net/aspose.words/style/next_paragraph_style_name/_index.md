---
title: next_paragraph_style_name property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style."
type: docs
weight: 120
url: /python-net/aspose.words/style/next_paragraph_style_name/
---

## Style.next_paragraph_style_name property

Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a
paragraph formatted with the specified style.

This property is not used by Aspose.Words. The next paragraph style will only
be applied automatically when you edit the document in MS Word.


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

