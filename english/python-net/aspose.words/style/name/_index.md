---
title: Style.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Style.name property. Gets or sets the name of the style."
type: docs
weight: 130
url: /python-net/aspose.words/style/name/
---

## Style.name property

Gets or sets the name of the style.

Can not be empty string.

If there already is a style with such name in the collection, then this style will override it. All affected nodes will reference new style.




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

Shows how to clone a document's style.

```python
doc = aw.Document()

# The add_copy method creates a copy of the specified style and
# automatically generates a new name for the style, such as "Heading 1_0".
new_style = doc.styles.add_copy(doc.styles.get_by_name("Heading 1"))

# Use the style's "name" property to change the style's identifying name.
new_style.name = "My Heading 1"

# Our document now has two identical looking styles with different names.
# Changing settings of one of the styles do not affect the other.
new_style.font.color = drawing.Color.red

self.assertEqual("My Heading 1", new_style.name)
self.assertEqual("Heading 1", doc.styles.get_by_name("Heading 1").name)

self.assertEqual(doc.styles.get_by_name("Heading 1").type, new_style.type)
self.assertEqual(doc.styles.get_by_name("Heading 1").font.name, new_style.font.name)
self.assertEqual(doc.styles.get_by_name("Heading 1").font.size, new_style.font.size)
self.assertNotEqual(doc.styles.get_by_name("Heading 1").font.color, new_style.font.color)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

