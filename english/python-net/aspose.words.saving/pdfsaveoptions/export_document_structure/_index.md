---
title: PdfSaveOptions.export_document_structure property
linktitle: export_document_structure property
articleTitle: export_document_structure property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.export_document_structure property. Gets or sets a value determining whether or not to export document structure."
type: docs
weight: 140
url: /python-net/aspose.words.saving/pdfsaveoptions/export_document_structure/
---

## PdfSaveOptions.export_document_structure property

Gets or sets a value determining whether or not to export document structure.


```python
@property
def export_document_structure(self) -> bool:
    ...

@export_document_structure.setter
def export_document_structure(self, value: bool):
    ...

```

### Remarks

This value is ignored when saving to PDF/A-1a, PDF/A-2a and PDF/UA-1 because document structure is required for this compliance.

Note that exporting the document structure significantly increases the memory consumption, especially
for the large documents.




### Examples

Shows how to preserve document structure elements, which can assist in programmatically interpreting our document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Set the "ExportDocumentStructure" property to "true" to make the document structure, such tags, available via the
# "Content" navigation pane of Adobe Acrobat at the cost of increased file size.
# Set the "ExportDocumentStructure" property to "false" to not export the document structure.
options.export_document_structure = export_document_structure
# Suppose we export document structure while saving this document. In that case,
# we can open it using Adobe Acrobat and find tags for elements such as the heading
# and the next paragraph via "View" -> "Show/Hide" -> "Navigation panes" -> "Tags".
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportDocumentStructure.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

