---
title: Document.page_count property
linktitle: page_count property
articleTitle: page_count property
second_title: Aspose.Words for Python
description: "Document.page_count property. Gets the number of pages in the document as calculated by the most recent page layout operation."
type: docs
weight: 330
url: /es/python-net/aspose.words/document/page_count/
---

## Document.page_count property

Gets the number of pages in the document as calculated by the most recent page layout operation.


```python
@property
def page_count(self) -> int:
    ...

```

### Examples

Shows how to count the number of pages in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Page 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Page 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Page 3')
# Verifique el recuento de páginas esperado del documento.
self.assertEqual(3, doc.page_count)
# Obtener la propiedad PageCount invocó el diseño de página del documento para calcular el valor.
# Esta operación no necesitará repetirse al renderizar el documento a un formato de guardado de página fija,
# como .pdf. Así que puede ahorrar tiempo, especialmente con documentos más complejos.
doc.save(file_name=ARTIFACTS_DIR + 'Document.GetPageCount.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.update_page_layout()](../update_page_layout/#default)

