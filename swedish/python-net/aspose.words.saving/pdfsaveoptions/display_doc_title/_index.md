---
title: PdfSaveOptions.display_doc_title property
linktitle: display_doc_title property
articleTitle: display_doc_title property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.display_doc_title property. A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary."
type: docs
weight: 90
url: /sv/python-net/aspose.words.saving/pdfsaveoptions/display_doc_title/
---

## PdfSaveOptions.display_doc_title property

A flag specifying whether the window’s title bar should display the document title taken from
the Title entry of the document information dictionary.


```python
@property
def display_doc_title(self) -> bool:
    ...

@display_doc_title.setter
def display_doc_title(self, value: bool):
    ...

```

### Remarks

If ``False``, the title bar should instead display the name of the PDF file containing the document.

This flag is required by PDF/UA compliance. ``True`` value will be used automatically when saving
to PDF/UA.

The default value is ``False``.




### Examples

Shows how to display the title of the document as the title bar.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
doc.built_in_document_properties.title = 'Windows bar pdf title'
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
# Ställ in "DisplayDocTitle" till "true" för att få vissa PDF‑läsare, såsom Adobe Acrobat Pro,
# att visa värdet av dokumentets inbyggda egenskap "Title" i fliken som tillhör detta dokument.
# Ställ in "DisplayDocTitle" till "false" för att få sådana läsare att visa dokumentets filnamn.
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.display_doc_title = display_doc_title
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DocTitle.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

