---
title: TxtSaveOptionsBase.force_page_breaks property
linktitle: force_page_breaks property
articleTitle: force_page_breaks property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.force_page_breaks property. Allows to specify whether the page breaks should be preserved during export."
type: docs
weight: 30
url: /es/python-net/aspose.words.saving/txtsaveoptionsbase/force_page_breaks/
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
# Cree un objeto "TxtSaveOptions", que podemos pasar al método "Save" del documento
# método para modificar cómo guardamos el documento como texto sin formato.
save_options = aw.saving.TxtSaveOptions()
# Los objetos "Document" de Aspose.Words tienen saltos de página, al igual que los documentos de Microsoft Word.
# Los formatos de guardado como ".txt" son un cuerpo continuo de texto sin saltos de página.
# Establezca la propiedad "ForcePageBreaks" a "true" para conservar todos los saltos de página en forma de caracteres '\\f'.
# Establezca la propiedad "ForcePageBreaks" a "false" para descartar todos los saltos de página.
save_options.force_page_breaks = force_page_breaks
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt', save_options=save_options)
# Si cargamos un documento de texto sin formato con saltos de página,
# el objeto "Document" los usará para dividir el cuerpo en páginas.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt')
self.assertEqual(3 if force_page_breaks else 1, doc.page_count)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

