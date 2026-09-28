---
title: OutlineOptions.default_bookmarks_outline_level property
linktitle: default_bookmarks_outline_level property
articleTitle: default_bookmarks_outline_level property
second_title: Aspose.Words for Python
description: "OutlineOptions.default_bookmarks_outline_level property. Specifies the default level in the document outline at which to display Word bookmarks."
type: docs
weight: 50
url: /de/python-net/aspose.words.saving/outlineoptions/default_bookmarks_outline_level/
---

## OutlineOptions.default_bookmarks_outline_level property

Specifies the default level in the document outline at which to display Word bookmarks.


```python
@property
def default_bookmarks_outline_level(self) -> int:
    ...

@default_bookmarks_outline_level.setter
def default_bookmarks_outline_level(self, value: int):
    ...

```

### Remarks

Individual bookmarks level could be specified using [OutlineOptions.bookmarks_outline_levels](../bookmarks_outline_levels/) property.

Specify 0 and Word bookmarks will not be displayed in the document outline.
Specify 1 and Word bookmarks will be displayed in the document outline at level 1; 2 for level 2 and so on.

Default is 0. Valid range is 0 to 9.




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
* class [OutlineOptions](../)

