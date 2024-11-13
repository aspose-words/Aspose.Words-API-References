---
title: RevisionCollection.accept_all method
linktitle: accept_all method
articleTitle: accept_all method
second_title: Aspose.Words for Python
description: "RevisionCollection.accept_all method. Accepts all revisions in this collection."
type: docs
weight: 50
url: /python-net/aspose.words/revisioncollection/accept_all/
---

## accept_all() {#default}

Accepts all revisions in this collection.


```python
def accept_all(self):
    ...
```

### Examples

Shows how to compare documents.

```python
doc_original = aw.Document()
builder = aw.DocumentBuilder(doc=doc_original)
builder.writeln('This is the original document.')
doc_edited = aw.Document()
builder = aw.DocumentBuilder(doc=doc_edited)
builder.writeln('This is the edited document.')
# Comparing documents with revisions will throw an exception.
if doc_original.revisions.count == 0 and doc_edited.revisions.count == 0:
    doc_original.compare(document=doc_edited, author='authorName', date_time=datetime.datetime.now())
# After the comparison, the original document will gain a new revision
# for every element that is different in the edited document.
for r in doc_original.revisions:
    print(f'Revision type: {r.revision_type}, on a node of type "{r.parent_node.node_type}"')
    print(f'\tChanged text: "{r.parent_node.get_text()}"')
# Accepting these revisions will transform the original document into the edited document.
doc_original.revisions.accept_all()
self.assertEqual(doc_original.get_text(), doc_edited.get_text())
```

### See Also

* module [aspose.words](../../)
* class [RevisionCollection](../)

