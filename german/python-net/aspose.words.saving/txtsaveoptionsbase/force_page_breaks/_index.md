---
title: TxtSaveOptionsBase.force_page_breaks property
linktitle: force_page_breaks property
articleTitle: force_page_breaks property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.force_page_breaks property. Allows to specify whether the page breaks should be preserved during export."
type: docs
weight: 30
url: /de/python-net/aspose.words.saving/txtsaveoptionsbase/force_page_breaks/
---

## TxtSaveOptionsBase.force_page_breaks property

Allows to specify whether the page breaks should be preserved during export.

The default value is ``False``.




```python
@property
def force_page_breaks(self) -> bool:
    ...

@force_page_breaks.setter
def force_page_breaks(self, value: bool):
    ...

```

### Remarks

The property affects only page breaks that are inserted explicitly into a document. 
It is not related to page breaks that MS Word automatically inserts at the end of each page.


### Examples

Shows how to specify whether to preserve page breaks when exporting a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Page 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3')
# Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
# Methode, um zu ändern, wie wir das Dokument als Klartext speichern.
save_options = aw.saving.TxtSaveOptions()
# Die Aspose.Words "Document"-Objekte haben Seitenumbrüche, genau wie Microsoft Word-Dokumente.
# Speicherformate wie ".txt" sind ein zusammenhängender Textkörper ohne Seitenumbrüche.
# Setzen Sie die "ForcePageBreaks"-Eigenschaft auf "true", um alle Seitenumbrüche in Form von '\f'-Zeichen zu erhalten.
# Setzen Sie die "ForcePageBreaks"-Eigenschaft auf "false", um alle Seitenumbrüche zu verwerfen.
save_options.force_page_breaks = force_page_breaks
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt', save_options=save_options)
# Wenn wir ein Klartextdokument mit Seitenumbrüchen laden,
# wird das "Document"-Objekt sie verwenden, um den Inhalt in Seiten zu unterteilen.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt')
self.assertEqual(3 if force_page_breaks else 1, doc.page_count)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

