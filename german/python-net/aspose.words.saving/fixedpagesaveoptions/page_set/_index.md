---
title: FixedPageSaveOptions.page_set property
linktitle: page_set property
articleTitle: page_set property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.page_set property. Gets or sets the pages to render"
type: docs
weight: 70
url: /de/python-net/aspose.words.saving/fixedpagesaveoptions/page_set/
---

## FixedPageSaveOptions.page_set property

Gets or sets the pages to render.
Default is all the pages in the document.


```python
@property
def page_set(self) -> aspose.words.saving.PageSet:
    ...

@page_set.setter
def page_set(self, value: aspose.words.saving.PageSet):
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

Shows how to extract pages based on exact page indices.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Füge dem Dokument fünf Seiten hinzu.
i = 1
while i < 6:
    builder.write('Page ' + str(i))
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Erstelle ein "XpsSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können.
# um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
xps_options = aw.saving.XpsSaveOptions()
# Verwende die "PageSet"-Eigenschaft, um eine Menge von Dokumentseiten auszuwählen, die als XPS ausgegeben werden sollen.
# In diesem Fall wählen wir über einen nullbasierten Index nur drei Seiten aus: Seite 1, Seite 2 und Seite 4.
xps_options.page_set = aw.saving.PageSet(pages=[0, 1, 3])
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.ExportExactPages.xps', save_options=xps_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

