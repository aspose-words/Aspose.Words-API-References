---
title: ImportFormatOptions class
linktitle: ImportFormatOptions class
articleTitle: ImportFormatOptions class
second_title: Aspose.Words for Python
description: "aspose.words.ImportFormatOptions class. Allows to specify various import options to format output"
type: docs
weight: 590
url: /python-net/aspose.words/importformatoptions/
---

## ImportFormatOptions class

Allows to specify various import options to format output.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/python-net/specify-load-options/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [ImportFormatOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [adjust_sentence_and_word_spacing](./adjust_sentence_and_word_spacing/) | Gets or sets a boolean value that specifies whether to adjust sentence and word spacing automatically. The default value is ``False``. |
| [force_copy_styles](./force_copy_styles/) | Gets or sets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP_SOURCE_FORMATTING](../importformatmode/#KEEP_SOURCE_FORMATTING) mode. The default value is ``False``. |
| [ignore_header_footer](./ignore_header_footer/) | Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP_SOURCE_FORMATTING](../importformatmode/#KEEP_SOURCE_FORMATTING) mode is used. The default value is ``True``. |
| [ignore_text_boxes](./ignore_text_boxes/) | Gets or sets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP_SOURCE_FORMATTING](../importformatmode/#KEEP_SOURCE_FORMATTING) mode is used. The default value is ``True``. |
| [keep_source_numbering](./keep_source_numbering/) | Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. The default value is ``False``. |
| [merge_pasted_lists](./merge_pasted_lists/) | Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is ``False``. |
| [smart_style_behavior](./smart_style_behavior/) | Gets or sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. The default value is ``False``. |

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

* module [aspose.words](../)

