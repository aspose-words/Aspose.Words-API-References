---
title: StyleCollection.default_font property
linktitle: default_font property
articleTitle: default_font property
second_title: Aspose.Words for Python
description: "StyleCollection.default_font property. Gets document default text formatting."
type: docs
weight: 30
url: /python-net/aspose.words/stylecollection/default_font/
---

## StyleCollection.default_font property

Gets document default text formatting.


```python
@property
def default_font(self) -> aspose.words.Font:
    ...

```

### Remarks

Note that document-wide defaults were introduced in Microsoft Word 2007 and are fully supported in OOXML formats ([LoadFormat.DOCX](../../loadformat/#DOCX)) only.
Earlier document formats have limited support for this feature and only font names can be stored.




### Examples

Shows how to add a Style to a document's styles collection.

```python
doc = aw.Document()
styles = doc.styles

# Set default parameters for new styles that we may later add to this collection.
styles.default_font.name = "Courier New"

# If we add a style of the "StyleType.PARAGRAPH", the collection will apply the values of
# its "default_paragraph_format" property to the style's "paragraph_format" property.
styles.default_paragraph_format.first_line_indent = 15.0

# Add a style, and then verify that it has the default settings.
styles.add(aw.StyleType.PARAGRAPH, "MyStyle")

self.assertEqual("Courier New", styles[4].font.name)
self.assertEqual(15.0, styles.get_by_name("MyStyle").paragraph_format.first_line_indent)
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

