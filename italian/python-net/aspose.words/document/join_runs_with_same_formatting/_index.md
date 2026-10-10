---
title: Document.join_runs_with_same_formatting method
linktitle: join_runs_with_same_formatting method
articleTitle: join_runs_with_same_formatting method
second_title: Aspose.Words for Python
description: "Document.join_runs_with_same_formatting method. Joins runs with same formatting in all paragraphs of the document."
type: docs
weight: 670
url: /it/python-net/aspose.words/document/join_runs_with_same_formatting/
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
# Apri un documento che contiene sequenze di testo adiacenti con formattazione identica,
# che si verifica comunemente se modifichiamo lo stesso paragrafo più volte in Microsoft Word.
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Se un numero qualsiasi di queste sequenze è adiacente con formattazione identica,
# allora il documento può essere semplificato.
self.assertEqual(317, doc.get_child_nodes(aw.NodeType.RUN, True).count)
# Combina tali sequenze con questo metodo e verifica il numero di unioni di sequenze che avranno luogo.
self.assertEqual(121, doc.join_runs_with_same_formatting())
# Il numero di unioni e il numero di sequenze che abbiamo dopo l'unione
# dovrebbero sommarsi al numero di sequenze che avevamo inizialmente.
self.assertEqual(196, doc.get_child_nodes(aw.NodeType.RUN, True).count)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

