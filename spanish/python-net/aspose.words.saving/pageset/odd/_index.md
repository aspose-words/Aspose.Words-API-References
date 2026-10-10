---
title: PageSet.odd property
linktitle: odd property
articleTitle: odd property
second_title: Aspose.Words for Python
description: "PageSet.odd property. Gets a set with all the odd pages of the document in their original order."
type: docs
weight: 40
url: /es/python-net/aspose.words.saving/pageset/odd/
---

## PageSet.odd property

Gets a set with all the odd pages of the document in their original order.


```python
@property
def odd(self) -> aspose.words.saving.PageSet:
    ...

```

### Remarks

Odd pages have even indices since page indices are zero-based.


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
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# A continuación se presentan tres propiedades PageSet que podemos usar para filtrar un conjunto de páginas de
# nuestro documento para guardarlas en un documento PDF de salida según la paridad de sus números de página.
# 1 -  Guardar solo las páginas pares:
options.page_set = aw.saving.PageSet.even
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Even.pdf', save_options=options)
# 2 -  Guardar solo las páginas impares:
options.page_set = aw.saving.PageSet.odd
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Odd.pdf', save_options=options)
# 3 -  Guardar cada página:
options.page_set = aw.saving.PageSet.all
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.All.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PageSet](../)

