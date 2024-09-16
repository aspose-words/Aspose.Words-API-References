---
title: ImportFormatOptions.adjust_sentence_and_word_spacing property
linktitle: adjust_sentence_and_word_spacing property
articleTitle: adjust_sentence_and_word_spacing property
second_title: Aspose.Words for Python
description: "ImportFormatOptions.adjust_sentence_and_word_spacing property. Gets or sets a boolean value that specifies whether to adjust sentence and word spacing automatically"
type: docs
weight: 20
url: /python-net/aspose.words/importformatoptions/adjust_sentence_and_word_spacing/
---

## ImportFormatOptions.adjust_sentence_and_word_spacing property

Gets or sets a boolean value that specifies whether to adjust sentence and word spacing automatically.
The default value is ``False``.



```python
@property
def adjust_sentence_and_word_spacing(self) -> bool:
    ...

@adjust_sentence_and_word_spacing.setter
def adjust_sentence_and_word_spacing(self, value: bool):
    ...

```

### Examples

Shows how to adjust sentence and word spacing automatically.

```python
src_doc = aw.Document()
dst_doc = aw.Document()
builder = aw.DocumentBuilder(doc=src_doc)
builder.write('Dolor sit amet.')
builder = aw.DocumentBuilder(doc=dst_doc)
builder.write('Lorem ipsum.')
options = aw.ImportFormatOptions()
options.adjust_sentence_and_word_spacing = True
builder.insert_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.USE_DESTINATION_STYLES, import_format_options=options)
self.assertEqual('Lorem ipsum. Dolor sit amet.', dst_doc.first_section.body.first_paragraph.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

