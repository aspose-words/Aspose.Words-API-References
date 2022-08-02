---
title: duplicate_style property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets/sets a flag indicating whether duplicate styles should be removed from document"
type: docs
weight: 20
url: /python-net/aspose.words/cleanupoptions/duplicate_style/
---

## CleanupOptions.duplicate_style property

Gets/sets a flag indicating whether duplicate styles should be removed from document.
Default value is **false**.



### Examples

Shows how to remove duplicated styles from the document.

```python
doc = aw.Document()

# Add two styles to the document with identical properties,
# but different names. The second style is considered a duplicate of the first.
my_style = doc.styles.add(aw.StyleType.PARAGRAPH, "MyStyle1")
my_style.font.size = 14
my_style.font.name = "Courier New"
my_style.font.color = drawing.Color.blue

duplicate_style = doc.styles.add(aw.StyleType.PARAGRAPH, "MyStyle2")
duplicate_style.font.size = 14
duplicate_style.font.name = "Courier New"
duplicate_style.font.color = drawing.Color.blue

self.assertEqual(6, doc.styles.count)

# Apply both styles to different paragraphs within the document.
builder = aw.DocumentBuilder(doc)
builder.paragraph_format.style_name = my_style.name
builder.writeln("Hello world!")

builder.paragraph_format.style_name = duplicate_style.name
builder.writeln("Hello again!")

paragraphs = doc.first_section.body.paragraphs

self.assertEqual(my_style, paragraphs[0].paragraph_format.style)
self.assertEqual(duplicate_style, paragraphs[1].paragraph_format.style)

# Configure a CleanOptions object, then call the "cleanup" method to substitute all duplicate styles
# with the original and remove the duplicates from the document.
cleanup_options = aw.CleanupOptions()
cleanup_options.duplicate_style = True

doc.cleanup(cleanup_options)

self.assertEqual(5, doc.styles.count)
self.assertEqual(my_style, paragraphs[0].paragraph_format.style)
self.assertEqual(my_style, paragraphs[1].paragraph_format.style)
```

### See Also

* module [aspose.words](../../)
* class [CleanupOptions](../)

