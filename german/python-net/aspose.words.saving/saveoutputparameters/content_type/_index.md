---
title: SaveOutputParameters.content_type property
linktitle: content_type property
articleTitle: content_type property
second_title: Aspose.Words for Python
description: "SaveOutputParameters.content_type property. Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document."
type: docs
weight: 10
url: /de/python-net/aspose.words.saving/saveoutputparameters/content_type/
---

## SaveOutputParameters.content_type property

Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document.


```python
@property
def content_type(self) -> str:
    ...

```

### Examples

Shows how to access output parameters of a document's save operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Nachdem wir ein Dokument gespeichert haben, können wir den Internet Media Type (MIME-Typ) des neu erstellten Ausgabedokuments abrufen.
parameters = doc.save(file_name=ARTIFACTS_DIR + 'Document.SaveOutputParameters.doc')
self.assertEqual('application/msword', parameters.content_type)
# Diese Eigenschaft ändert sich je nach Speicherformat.
parameters = doc.save(file_name=ARTIFACTS_DIR + 'Document.SaveOutputParameters.pdf')
self.assertEqual('application/pdf', parameters.content_type)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOutputParameters](../)

