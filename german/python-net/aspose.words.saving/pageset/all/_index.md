---
title: PageSet.all property
linktitle: all property
articleTitle: all property
second_title: Aspose.Words for Python
description: "PageSet.all property. Gets a set with all the pages of the document in their original order."
type: docs
weight: 20
url: /de/python-net/aspose.words.saving/pageset/all/
---

## PageSet.all property

Gets a set with all the pages of the document in their original order.


```python
@property
def all(self) -> aspose.words.saving.PageSet:
    ...

```

### Examples

Shows how to export Odd pages from the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 5:
    builder.writeln(f"Page {i + 1} ({('odd' if i % 2 == 0 else 'even')})")
    if i < 4:
        builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Unten sind drei PageSet-Eigenschaften, die wir verwenden können, um einen Satz von Seiten aus
# unserem Dokument zu speichern, in ein Ausgabepdf-Dokument, basierend auf der Parität ihrer Seitenzahlen.
# 1 -  Speichern Sie nur die geraden Seiten:
options.page_set = aw.saving.PageSet.even
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Even.pdf', save_options=options)
# 2 -  Speichern Sie nur die ungeraden Seiten:
options.page_set = aw.saving.PageSet.odd
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Odd.pdf', save_options=options)
# 3 -  Jede Seite speichern:
options.page_set = aw.saving.PageSet.all
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.All.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PageSet](../)

