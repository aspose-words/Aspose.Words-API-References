---
title: Document.page_count property
linktitle: page_count property
articleTitle: page_count property
second_title: Aspose.Words for Python
description: "Document.page_count property. Gets the number of pages in the document as calculated by the most recent page layout operation."
type: docs
weight: 330
url: /de/python-net/aspose.words/document/page_count/
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
# Überprüfen Sie die erwartete Seitenzahl des Dokuments.
self.assertEqual(3, doc.page_count)
# Das Abrufen der PageCount-Eigenschaft löste das Seitenlayout des Dokuments aus, um den Wert zu berechnen.
# Dieser Vorgang muss beim Rendern des Dokuments in ein festes Seitenformat nicht erneut durchgeführt werden,
# wie .pdf. So können Sie Zeit sparen, insbesondere bei komplexeren Dokumenten.
doc.save(file_name=ARTIFACTS_DIR + 'Document.GetPageCount.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.update_page_layout()](../update_page_layout/#default)

