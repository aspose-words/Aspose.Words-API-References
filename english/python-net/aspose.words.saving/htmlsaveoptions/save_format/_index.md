---
title: save_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 440
url: /python-net/aspose.words.saving/htmlsaveoptions/save_format/
---

## HtmlSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can be [SaveFormat.HTML](../../../aspose.words/saveformat/#HTML), [SaveFormat.MHTML](../../../aspose.words/saveformat/#MHTML),
[SaveFormat.EPUB](../../../aspose.words/saveformat/#EPUB) or [SaveFormat.AZW3](../../../aspose.words/saveformat/#AZW3).



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

