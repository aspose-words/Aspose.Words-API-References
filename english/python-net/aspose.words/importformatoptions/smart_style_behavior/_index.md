---
title: smart_style_behavior property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents"
type: docs
weight: 80
url: /python-net/aspose.words/importformatoptions/smart_style_behavior/
---

## ImportFormatOptions.smart_style_behavior property

Gets or sets a boolean value that specifies how styles will be imported
when they have equal names in source and destination documents.
The default value is ``False``.


When this option is **enabled**, the source style will be expanded into a direct attributes inside a
destination document, if [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) importing mode is used.

When this option is **disabled**, the source style will be expanded only if it is numbered. Existing
destination attributes will not be overridden, including lists.




### Examples

Shows how to resolve duplicate styles while inserting documents.

```python
dst_doc = aw.Document()
builder = aw.DocumentBuilder(dst_doc)

my_style = builder.document.styles.add(aw.StyleType.PARAGRAPH, "MyStyle")
my_style.font.size = 14
my_style.font.name = "Courier New"
my_style.font.color = drawing.Color.blue

builder.paragraph_format.style_name = my_style.name
builder.writeln("Hello world!")

# Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
# If we insert the clone into the original document, the two styles with the same name will cause a clash.
src_doc = dst_doc.clone()
src_doc.styles.get_by_name("MyStyle").font.color = drawing.Color.red

# When we enable "smart_style_behavior" and use the KEEP_SOURCE_FORMATTING import format mode,
# Aspose.Words will resolve style clashes by converting source document styles.
# with the same names as destination styles into direct paragraph attributes.
options = aw.ImportFormatOptions()
options.smart_style_behavior = True

builder.insert_document(src_doc, aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, options)

dst_doc.save(ARTIFACTS_DIR + "DocumentBuilder.smart_style_behavior.docx")
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

