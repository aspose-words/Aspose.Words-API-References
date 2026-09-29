---
title: PageSet.all property
linktitle: all property
articleTitle: all property
second_title: Aspose.Words for Python
description: "PageSet.all property. Gets a set with all the pages of the document in their original order."
type: docs
weight: 20
url: /it/python-net/aspose.words.saving/pageset/all/
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
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
options = aw.saving.PdfSaveOptions()
# Di seguito sono riportate tre proprietà PageSet che possiamo usare per filtrare un insieme di pagine da
# il nostro documento da salvare in un PDF di output in base alla parità dei loro numeri di pagina.
# 1 -  Salva solo le pagine pari:
options.page_set = aw.saving.PageSet.even
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Even.pdf', save_options=options)
# 2 -  Salva solo le pagine dispari:
options.page_set = aw.saving.PageSet.odd
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Odd.pdf', save_options=options)
# 3 -  Salva ogni pagina:
options.page_set = aw.saving.PageSet.all
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.All.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PageSet](../)

