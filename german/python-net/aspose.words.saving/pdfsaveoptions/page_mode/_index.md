---
title: PdfSaveOptions.page_mode property
linktitle: page_mode property
articleTitle: page_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.page_mode property. Specifies how the PDF document should be displayed when opened in a PDF reader."
type: docs
weight: 280
url: /de/python-net/aspose.words.saving/pdfsaveoptions/page_mode/
---

## PdfSaveOptions.page_mode property

Specifies how the PDF document should be displayed when opened in a PDF reader.


```python
@property
def page_mode(self) -> aspose.words.saving.PdfPageMode:
    ...

@page_mode.setter
def page_mode(self, value: aspose.words.saving.PdfPageMode):
    ...

```

### Remarks

The default value is [PdfPageMode.USE_OUTLINES](../../pdfpagemode/#USE_OUTLINES).



### Examples

Shows to process bookmarks in headers/footers in a document that we are rendering to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'Bookmarks in headers and footers.docx')
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
save_options = aw.saving.PdfSaveOptions()
# Setzen Sie die Eigenschaft "PageMode" auf "PdfPageMode.UseOutlines", um das Gliederungs‑Navigationsfenster im ausgegebenen PDF anzuzeigen.
save_options.page_mode = aw.saving.PdfPageMode.USE_OUTLINES
# Setzen Sie die Eigenschaft "DefaultBookmarksOutlineLevel" auf "1", um alle
# Lesezeichen auf der ersten Ebene der Gliederung im ausgegebenen PDF anzuzeigen.
save_options.outline_options.default_bookmarks_outline_level = 1
# Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.None", um
# keine Lesezeichen zu exportieren, die sich in Kopf‑/Fußzeilen befinden.
# Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.First", um
# nur Lesezeichen im Kopf‑/Fußzeilenbereich des ersten Abschnitts zu exportieren.
# Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.All", um
# Lesezeichen zu exportieren, die sich in allen Kopf‑/Fußzeilen befinden.
save_options.header_footer_bookmarks_export_mode = header_footer_bookmarks_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

