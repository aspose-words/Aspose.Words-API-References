---
title: InlineStory.is_move_to_revision property
linktitle: is_move_to_revision property
articleTitle: is_move_to_revision property
second_title: Aspose.Words for Python
description: "InlineStory.is_move_to_revision property. Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 60
url: /it/python-net/aspose.words/inlinestory/is_move_to_revision/
---

## InlineStory.is_move_to_revision property

Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_to_revision(self) -> bool:
    ...

```

### Examples

Shows how to view revision-related properties of InlineStory nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision footnotes.docx')
# Quando modifichiamo il documento con l'opzione "Track Changes", trovata in Revisione -> Tracciamento,
# è attivata in Microsoft Word, le modifiche che applichiamo contano come revisioni.
# Durante la modifica di un documento con Aspose.Words, possiamo iniziare a tracciare le revisioni mediante
# invocando il metodo "StartTrackRevisions" del documento e interrompendo il tracciamento usando il metodo "StopTrackRevisions".
# Possiamo accettare le revisioni per assimilarle nel documento
# oppure rifiatarli per annullare e scartare la modifica proposta.
self.assertTrue(doc.has_revisions)
footnotes = list(map(lambda x: x.as_footnote(), list(doc.get_child_nodes(aw.NodeType.FOOTNOTE, True))))
self.assertEqual(5, len(footnotes))
# Di seguito sono cinque tipi di revisioni che possono contrassegnare un nodo InlineStory.
# 1 -  Una revisione "insert":
# Questa revisione si verifica quando inseriamo del testo mentre tracciamo le modifiche.
self.assertTrue(footnotes[2].is_insert_revision)
# 2 -  Una revisione "move from":
# Quando evidenziamo del testo in Microsoft Word e poi lo trasciniamo in una posizione diversa del documento
# mentre tracciamo le modifiche, compaiono due revisioni.
# La revisione "move from" è una copia del testo originale prima di spostarlo.
self.assertTrue(footnotes[4].is_move_from_revision)
# 3 -  Una revisione "move to":
# La revisione "move to" è il testo che abbiamo spostato nella sua nuova posizione nel documento.
# Le revisioni "Move from" e "move to" compaiono in coppia per ogni revisione di spostamento che eseguiamo.
# Accettare una revisione di spostamento elimina la revisione "move from" e il suo testo,
# e conserva il testo della revisione "move to".
# Rifiutare una revisione di spostamento, al contrario, mantiene la revisione "move from" ed elimina la revisione "move to".
self.assertTrue(footnotes[1].is_move_to_revision)
# 4 -  Una revisione "delete":
# Questa revisione si verifica quando eliminiamo del testo mentre tracciamo le modifiche. Quando eliminiamo il testo in questo modo,
# rimarrà nel documento come revisione finché non accetteremo la revisione,
# che eliminerà definitivamente il testo, o rifiuterà la revisione, che manterrà il testo che abbiamo eliminato al suo posto.
self.assertTrue(footnotes[3].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

