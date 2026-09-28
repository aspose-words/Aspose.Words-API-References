---
title: HeaderFooterBookmarksExportMode enumeration
linktitle: HeaderFooterBookmarksExportMode enumeration
articleTitle: HeaderFooterBookmarksExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.HeaderFooterBookmarksExportMode enumeration. Specifies how bookmarks in headers/footers are exported."
type: docs
weight: 220
url: /de/python-net/aspose.words.saving/headerfooterbookmarksexportmode/
---

## HeaderFooterBookmarksExportMode enumeration

Specifies how bookmarks in headers/footers are exported.


### Members

| Name | Description |
| --- | --- |
| NONE | Bookmarks in headers/footers are not exported. |
| FIRST | Only bookmark in first header/footer of the section is exported. |
| ALL | Bookmarks in all headers/footers are exported. |

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

* module [aspose.words.saving](../)

