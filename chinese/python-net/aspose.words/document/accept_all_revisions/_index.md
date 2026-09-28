---
title: Document.accept_all_revisions method
linktitle: accept_all_revisions method
articleTitle: accept_all_revisions method
second_title: Aspose.Words for Python
description: "Document.accept_all_revisions method. Accepts all tracked changes in the document."
type: docs
weight: 550
url: /zh/python-net/aspose.words/document/accept_all_revisions/
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
# 在跟踪更改的同时编辑文档，以创建几个修订。
doc.start_track_revisions(author='John Doe')
builder.write('Hello world! ')
builder.write('Hello again! ')
builder.write('This is another revision.')
doc.stop_track_revisions()
self.assertEqual(3, doc.revisions.count)
# 我们可以遍历每个修订，并在文档中接受或拒绝它。
# 如果我们知道想要接受所有修订，可以通过调用此方法更直接地完成。
doc.accept_all_revisions()
self.assertEqual(0, doc.revisions.count)
self.assertEqual('Hello world! Hello again! This is another revision.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

