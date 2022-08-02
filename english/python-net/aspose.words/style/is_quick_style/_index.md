---
title: is_quick_style property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether this style is shown in the Quick Style gallery inside MS Word UI."
type: docs
weight: 70
url: /python-net/aspose.words/style/is_quick_style/
---

## Style.is_quick_style property

Specifies whether this style is shown in the Quick Style gallery inside MS Word UI.


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

