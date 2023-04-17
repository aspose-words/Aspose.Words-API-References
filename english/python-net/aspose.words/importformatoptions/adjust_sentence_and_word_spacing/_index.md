---
title: adjust_sentence_and_word_spacing property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a boolean value that specifies whether to adjust sentence and word spacing automatically"
type: docs
weight: 20
url: /python-net/aspose.words/importformatoptions/adjust_sentence_and_word_spacing/
---

## ImportFormatOptions.adjust_sentence_and_word_spacing property

Gets or sets a boolean value that specifies whether to adjust sentence and word spacing automatically.
The default value is ``False``.



### Examples

Shows how to adjust sentence and word spacing automatically.

```python
srcDoc = aw.Document()
dstDoc = aw.Document()

builder = aw.DocumentBuilder(srcDoc)
builder.write("Dolor sit amet.")

builder = aw.DocumentBuilder(dstDoc)
builder.write("Lorem ipsum.")

options = aw.ImportFormatOptions()
options.adjust_sentence_and_word_spacing = True

builder.insert_document(srcDoc, aw.ImportFormatMode.USE_DESTINATION_STYLES, options)

self.assertEqual("Lorem ipsum. Dolor sit amet.", dstDoc.first_section.body.first_paragraph.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

