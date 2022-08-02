---
title: display_doc_title property
second_title: Aspose.Words for Python via .NET API Reference
description: "A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary."
type: docs
weight: 70
url: /python-net/aspose.words.saving/pdfsaveoptions/display_doc_title/
---

## PdfSaveOptions.display_doc_title property

A flag specifying whether the window’s title bar should display the document title taken from
the Title entry of the document information dictionary.

If ``false``, the title bar should instead display the name of the PDF file containing the document.

This flag is required by PDF/UA compliance. ``true`` value will be used automatically when saving
to PDF/UA.

The default value is ``false``.




### Examples

Shows how to display the title of the document as the title bar.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

doc.built_in_document_properties.title = "Windows bar pdf title"

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
# Set the "display_doc_title" to "True" to get some PDF readers, such as Adobe Acrobat Pro,
# to display the value of the document's "title" built-in property in the tab that belongs to this document.
# Set the "display_doc_title" to "False" to get such readers to display the document's filename.
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.display_doc_title = display_doc_title

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.doc_title.pdf", pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

