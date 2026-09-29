---
title: Revision.parent_node property
linktitle: parent_node property
articleTitle: parent_node property
second_title: Aspose.Words for Python
description: "Revision.parent_node property. Gets the immediate parent node (owner) of this revision"
type: docs
weight: 40
url: /it/python-net/aspose.words/revision/parent_node/
---

## Revision.parent_node property

Gets the immediate parent node (owner) of this revision.
This property will work for any revision type other than [RevisionType.STYLE_DEFINITION_CHANGE](../../revisiontype/#STYLE_DEFINITION_CHANGE).



```python
@property
def parent_node(self) -> aspose.words.Node:
    ...

```

### Remarks

If this revision relates to change of Style formatting, use [Revision.parent_style](../parent_style/) instead.



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

* module [aspose.words](../../)
* class [Revision](../)

