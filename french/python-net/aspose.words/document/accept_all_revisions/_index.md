---
title: Document.accept_all_revisions method
linktitle: accept_all_revisions method
articleTitle: accept_all_revisions method
second_title: Aspose.Words for Python
description: "Document.accept_all_revisions method. Accepts all tracked changes in the document."
type: docs
weight: 550
url: /fr/python-net/aspose.words/document/accept_all_revisions/
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
# Modifiez le document tout en suivant les modifications pour créer quelques révisions.
doc.start_track_revisions(author='John Doe')
builder.write('Hello world! ')
builder.write('Hello again! ')
builder.write('This is another revision.')
doc.stop_track_revisions()
self.assertEqual(3, doc.revisions.count)
# Nous pouvons parcourir chaque révision et l'accepter/rejeter dans le cadre de notre document.
# Si nous savons que nous souhaitons accepter chaque révision, nous pouvons le faire de manière plus simple en appelant cette méthode.
doc.accept_all_revisions()
self.assertEqual(0, doc.revisions.count)
self.assertEqual('Hello world! Hello again! This is another revision.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

