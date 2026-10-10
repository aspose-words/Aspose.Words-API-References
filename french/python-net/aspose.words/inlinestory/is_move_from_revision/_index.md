---
title: InlineStory.is_move_from_revision property
linktitle: is_move_from_revision property
articleTitle: is_move_from_revision property
second_title: Aspose.Words for Python
description: "InlineStory.is_move_from_revision property. Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 50
url: /fr/python-net/aspose.words/inlinestory/is_move_from_revision/
---

## InlineStory.is_move_from_revision property

Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_from_revision(self) -> bool:
    ...

```

### Examples

Shows how to view revision-related properties of InlineStory nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision footnotes.docx')
# Lorsque nous modifions le document alors que l'option "Track Changes", trouvée via Révision -> Suivi,
# est activée dans Microsoft Word, les modifications que nous appliquons sont comptées comme des révisions.
# Lors de la modification d'un document avec Aspose.Words, nous pouvons commencer à suivre les révisions en
# appelant la méthode "StartTrackRevisions" du document et en arrêtant le suivi en utilisant la méthode "StopTrackRevisions".
# Nous pouvons soit accepter les révisions pour les intégrer au document
# ou rejetez-les pour annuler et abandonner la modification proposée.
self.assertTrue(doc.has_revisions)
footnotes = list(map(lambda x: x.as_footnote(), list(doc.get_child_nodes(aw.NodeType.FOOTNOTE, True))))
self.assertEqual(5, len(footnotes))
# Voici cinq types de révisions pouvant marquer un nœud InlineStory.
# 1 -  Une révision "insert" :
# Cette révision se produit lorsque nous insérons du texte tout en suivant les modifications.
self.assertTrue(footnotes[2].is_insert_revision)
# 2 -  Une révision "move from" :
# Lorsque nous sélectionnons du texte dans Microsoft Word, puis le faisons glisser vers un autre emplacement du document
# tout en suivant les modifications, deux révisions apparaissent.
# La révision "move from" est une copie du texte original avant que nous le déplacions.
self.assertTrue(footnotes[4].is_move_from_revision)
# 3 -  Une révision "move to" :
# La révision "move to" est le texte que nous avons déplacé à sa nouvelle position dans le document.
# Les révisions "move from" et "move to" apparaissent par paires pour chaque révision de déplacement que nous effectuons.
# Accepter une révision de déplacement supprime la révision "move from" ainsi que son texte,
# et conserve le texte de la révision "move to".
# Rejeter une révision de déplacement conserve au contraire la révision "move from" et supprime la révision "move to".
self.assertTrue(footnotes[1].is_move_to_revision)
# 4 -  Une révision "delete" :
# Cette révision se produit lorsque nous supprimons du texte tout en suivant les modifications. Lorsque nous supprimons du texte de cette façon,
# il restera dans le document en tant que révision jusqu'à ce que nous l'acceptions ou le rejetions.
# qui supprimera le texte définitivement, ou rejettera la révision, ce qui gardera le texte que nous avons supprimé à son emplacement.
self.assertTrue(footnotes[3].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

