---
title: Document.join_runs_with_same_formatting method
linktitle: join_runs_with_same_formatting method
articleTitle: join_runs_with_same_formatting method
second_title: Aspose.Words for Python
description: "Document.join_runs_with_same_formatting method. Joins runs with same formatting in all paragraphs of the document."
type: docs
weight: 670
url: /de/python-net/aspose.words/document/join_runs_with_same_formatting/
---

## join_runs_with_same_formatting() {#default}

Joins runs with same formatting in all paragraphs of the document.


```python
def join_runs_with_same_formatting(self):
    ...
```

### Remarks

This is an optimization method. Some documents contain adjacent runs with same formatting.
Usually this occurs if a document was intensively edited manually.
You can reduce the document size and speed up further processing by joining these runs.

The operation checks every [Paragraph](../../paragraph/) node in the document for adjacent [Run](../../run/)
nodes having identical properties. It ignores unique identifiers used to track editing sessions of run
creation and modification. First run in every joining sequence accumulates all text. Remaining
runs are deleted from the document.




### Returns

Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.


### Examples

Shows how to join runs in a document to reduce unneeded runs.

```python
# Öffnen Sie ein Dokument, das benachbarte Textläufe mit identischer Formatierung enthält,
# was häufig vorkommt, wenn wir denselben Absatz mehrfach in Microsoft Word bearbeiten.
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Wenn eine beliebige Anzahl dieser Läufe benachbart mit identischer Formatierung ist,
# kann das Dokument vereinfacht werden.
self.assertEqual(317, doc.get_child_nodes(aw.NodeType.RUN, True).count)
# Kombinieren Sie solche Läufe mit dieser Methode und überprüfen Sie die Anzahl der Laufzusammenführungen, die stattfinden werden.
self.assertEqual(121, doc.join_runs_with_same_formatting())
# Die Anzahl der Zusammenführungen und die Anzahl der Läufe, die wir nach der Zusammenführung haben
# sollte der Anzahl der Läufe entsprechen, die wir ursprünglich hatten.
self.assertEqual(196, doc.get_child_nodes(aw.NodeType.RUN, True).count)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

