---
title: HtmlSaveOptions.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.encoding property. Specifies the encoding to use when exporting to HTML, MHTML or EPUB"
type: docs
weight: 100
url: /python-net/aspose.words.saving/htmlsaveoptions/encoding/
---

## HtmlSaveOptions.encoding property

Specifies the encoding to use when exporting to HTML, MHTML or EPUB.
Default value is ``new UTF8Encoding(false)`` (UTF-8 without BOM).



```python
@property
def encoding(self) -> str:
    ...

@encoding.setter
def encoding(self, value: str):
    ...

```

### Remarks




### Examples

Shows how to use a specific encoding when saving a document to .epub.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# Use a SaveOptions object to specify the encoding for a document that we will save.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = "utf-8"

# By default, an output .epub document will have all its contents in one HTML part.
# A split criterion allows us to segment the document into several HTML parts.
# We will set the criteria to split the document into heading paragraphs.
# This is useful for readers who cannot read HTML files more significant than a specific size.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH

# Specify that we want to export document properties.
save_options.export_document_properties = True

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.doc2_epub_save_options.epub", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

