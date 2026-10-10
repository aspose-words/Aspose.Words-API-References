---
title: RunCollection class
linktitle: RunCollection class
articleTitle: RunCollection class
second_title: Aspose.Words for Python
description: "aspose.words.RunCollection class. Provides typed access to a collection of [Run](../run/) nodes"
type: docs
weight: 1120
url: /it/python-net/aspose.words/runcollection/
---

## RunCollection class

Provides typed access to a collection of [Run](../run/) nodes.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




**Inheritance:** [RunCollection](./) → [NodeCollection](../nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [Run](../run/) at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](../nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ clear()](../nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ contains(node)](../nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ index_of(node)](../nodecollection/index_of/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ insert(index, node)](../nodecollection/insert/#int_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove(node)](../nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove_at(index)](../nodecollection/remove_at/#int) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ to_array()](./to_array/#default) | Copies all runs from the collection to a new array of runs. |

### Examples

Shows how to determine the revision type of an inline node.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision runs.docx')
# Quando modifichiamo il documento con l'opzione "Track Changes", trovata in Revisione -> Tracciamento,
# è attivata in Microsoft Word, le modifiche che applichiamo contano come revisioni.
# Durante la modifica di un documento con Aspose.Words, possiamo iniziare a tracciare le revisioni mediante
# invocando il metodo "StartTrackRevisions" del documento e interrompendo il tracciamento usando il metodo "StopTrackRevisions".
# Possiamo accettare le revisioni per assimilarle nel documento
# oppure rifiutarle per modificare efficacemente la modifica proposta.
self.assertEqual(6, doc.revisions.count)
# Il nodo padre di una revisione è il run a cui la revisione si riferisce. Un Run è un nodo Inline.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# Di seguito sono riportati cinque tipi di revisioni che possono contrassegnare un nodo Inline.
# 1 -  Una revisione "insert":
# Questa revisione si verifica quando inseriamo del testo mentre tracciamo le modifiche.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  Una revisione "format":
# Questa revisione si verifica quando modifichiamo la formattazione del testo mentre tracciamo le modifiche.
self.assertTrue(runs[2].is_format_revision)
# 3 -  Una revisione "move from":
# Quando evidenziamo del testo in Microsoft Word e poi lo trasciniamo in una posizione diversa del documento
# mentre tracciamo le modifiche, compaiono due revisioni.
# La revisione "move from" è una copia del testo originale prima di spostarlo.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  Una revisione "move to":
# La revisione "move to" è il testo che abbiamo spostato nella sua nuova posizione nel documento.
# Le revisioni "Move from" e "move to" compaiono in coppia per ogni revisione di spostamento che eseguiamo.
# Accettare una revisione di spostamento elimina la revisione "move from" e il suo testo,
# e conserva il testo della revisione "move to".
# Rifiutare una revisione di spostamento, al contrario, mantiene la revisione "move from" ed elimina la revisione "move to".
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  Una revisione "delete":
# Questa revisione si verifica quando eliminiamo del testo mentre tracciamo le modifiche. Quando eliminiamo il testo in questo modo,
# rimarrà nel documento come revisione finché non accetteremo la revisione,
# che eliminerà definitivamente il testo, o rifiuterà la revisione, che manterrà il testo che abbiamo eliminato al suo posto.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../)
* class [NodeCollection](../nodecollection/)

