---
title: Document.page_count property
linktitle: page_count property
articleTitle: page_count property
second_title: Aspose.Words for Python
description: "Document.page_count property. Gets the number of pages in the document as calculated by the most recent page layout operation."
type: docs
weight: 330
url: /it/python-net/aspose.words/document/page_count/
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
# Verifica il conteggio delle pagine previsto del documento.
self.assertEqual(3, doc.page_count)
# Ottenere la proprietà PageCount ha attivato il layout di pagina del documento per calcolare il valore.
# Questa operazione non dovrà essere ripetuta durante il rendering del documento in un formato di salvataggio a pagina fissa,
# come .pdf. Così puoi risparmiare tempo, soprattutto con documenti più complessi.
doc.save(file_name=ARTIFACTS_DIR + 'Document.GetPageCount.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.update_page_layout()](../update_page_layout/#default)

