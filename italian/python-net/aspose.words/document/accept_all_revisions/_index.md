---
title: Document.accept_all_revisions method
linktitle: accept_all_revisions method
articleTitle: accept_all_revisions method
second_title: Aspose.Words for Python
description: "Document.accept_all_revisions method. Accepts all tracked changes in the document."
type: docs
weight: 550
url: /it/python-net/aspose.words/document/accept_all_revisions/
---

## accept_all_revisions() {#default}

Accepts all tracked changes in the document.


```python
def accept_all_revisions(self):
    ...
```

### Remarks

This method is a shortcut for [RevisionCollection.accept_all()](../../revisioncollection/accept_all/#default).


### Examples

Shows how to accept all tracking changes in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Modifica il documento tracciando le modifiche per creare alcune revisioni.
doc.start_track_revisions(author='John Doe')
builder.write('Hello world! ')
builder.write('Hello again! ')
builder.write('This is another revision.')
doc.stop_track_revisions()
self.assertEqual(3, doc.revisions.count)
# Possiamo iterare su ogni revisione e accettarla/rifiutarla come parte del nostro documento.
# Se sappiamo di voler accettare ogni revisione, possiamo farlo in modo più diretto chiamando questo metodo.
doc.accept_all_revisions()
self.assertEqual(0, doc.revisions.count)
self.assertEqual('Hello world! Hello again! This is another revision.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

