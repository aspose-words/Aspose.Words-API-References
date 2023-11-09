---
title: PdfSaveOptions.export_language_to_span_tag property
linktitle: export_language_to_span_tag property
articleTitle: export_language_to_span_tag property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.export_language_to_span_tag property. Gets or sets a value determining whether or not to create a Span tag in the document structure to export the text language."
type: docs
weight: 150
url: /python-net/aspose.words.saving/pdfsaveoptions/export_language_to_span_tag/
---

## PdfSaveOptions.export_language_to_span_tag property

Gets or sets a value determining whether or not to create a "Span" tag in the document structure to export the text language.


```python
@property
def export_language_to_span_tag(self) -> bool:
    ...

@export_language_to_span_tag.setter
def export_language_to_span_tag(self, value: bool):
    ...

```

### Remarks

Default value is ``False`` and "Lang" attribute is attached to a marked-content sequence in a page content stream.

When the value is ``True`` "Span" tag is created for the text with non-default language
and "Lang" attribute is attached to this tag.

This value is ignored when [PdfSaveOptions.export_document_structure](../export_document_structure/) is ``False``. 




### Examples

Shows how to create a "Span" tag in the document structure to export the text language.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")
builder.writeln("Hola mundo!")

save_options = aw.saving.PdfSaveOptions()

# Note, when "export_document_structure" is "False", "export_language_to_span_tag" is ignored.
save_options.export_document_structure = True
save_options.export_language_to_span_tag = True

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.export_language_to_span_tag.pdf", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

