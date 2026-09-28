---
title: Inline.parent_paragraph property
linktitle: parent_paragraph property
articleTitle: parent_paragraph property
second_title: Aspose.Words for Python
description: "Inline.parent_paragraph property. Retrieves the parent [Paragraph](../../paragraph/) of this node."
type: docs
weight: 70
url: /fr/python-net/aspose.words/inline/parent_paragraph/
---

## Inline.parent_paragraph property

Retrieves the parent [Paragraph](../../paragraph/) of this node.



```python
@property
def parent_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to determine the revision type of an inline node.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision runs.docx')
# Lorsque nous modifions le document alors que l'option "Track Changes", trouvée via Révision -> Suivi,
# est activée dans Microsoft Word, les modifications que nous appliquons sont comptées comme des révisions.
# Lors de la modification d'un document avec Aspose.Words, nous pouvons commencer à suivre les révisions en
# appelant la méthode "StartTrackRevisions" du document et en arrêtant le suivi en utilisant la méthode "StopTrackRevisions".
# Nous pouvons soit accepter les révisions pour les intégrer au document
# ou les rejeter afin de modifier efficacement le changement proposé.
self.assertEqual(6, doc.revisions.count)
# Le nœud parent d'une révision est le run auquel la révision se rapporte. Un Run est un nœud Inline.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# Voici cinq types de révisions pouvant marquer un nœud Inline.
# 1 -  Une révision "insert" :
# Cette révision se produit lorsque nous insérons du texte tout en suivant les modifications.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  Une révision "format" :
# Cette révision se produit lorsque nous modifions le formatage du texte tout en suivant les modifications.
self.assertTrue(runs[2].is_format_revision)
# 3 -  Une révision "move from" :
# Lorsque nous sélectionnons du texte dans Microsoft Word, puis le faisons glisser vers un autre emplacement du document
# tout en suivant les modifications, deux révisions apparaissent.
# La révision "move from" est une copie du texte original avant que nous le déplacions.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  Une révision "move to" :
# La révision "move to" est le texte que nous avons déplacé à sa nouvelle position dans le document.
# Les révisions "move from" et "move to" apparaissent par paires pour chaque révision de déplacement que nous effectuons.
# Accepter une révision de déplacement supprime la révision "move from" ainsi que son texte,
# et conserve le texte de la révision "move to".
# Rejeter une révision de déplacement conserve au contraire la révision "move from" et supprime la révision "move to".
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  Une révision "delete" :
# Cette révision se produit lorsque nous supprimons du texte tout en suivant les modifications. Lorsque nous supprimons du texte de cette façon,
# il restera dans le document en tant que révision jusqu'à ce que nous l'acceptions ou le rejetions.
# qui supprimera le texte définitivement, ou rejettera la révision, ce qui gardera le texte que nous avons supprimé à son emplacement.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [Inline](../)

