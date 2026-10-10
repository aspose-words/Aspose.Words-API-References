---
title: RevisionCollection.reject_all method
linktitle: reject_all method
articleTitle: reject_all method
second_title: Aspose.Words for Python
description: "RevisionCollection.reject_all method. Rejects all revisions in this collection."
type: docs
weight: 70
url: /fr/python-net/aspose.words/revisioncollection/reject_all/
---

## reject_all() {#default}

Rejects all revisions in this collection.


```python
def reject_all(self):
    ...
```

### Examples

Shows how to work with a document's collection of revisions.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
revisions = doc.revisions
# Cette collection possède elle-même une collection de groupes de révisions.
# Chaque groupe est une séquence de révisions adjacentes.
group_count = sum((1 for _ in revisions.groups))
print(f'{group_count} revision groups:')
# Itérez sur la collection de groupes et affichez le texte auquel la révision se rapporte.
for group in revisions.groups:
    print(f'\tGroup type "{group.revision_type}", ' + f'author: {group.author}, contents: [{group.text.strip()}]')
# Chaque Run qu’une révision affecte obtient un objet Revision correspondant.
# La collection de révisions est considérablement plus grande que la forme condensée que nous avons affichée ci‑dessus,
# en fonction du nombre de Runs que nous avons segmentés dans le document lors de l’édition avec Microsoft Word.
revision_count = sum((1 for _ in revisions))
print(f'\n{revision_count} revisions:')
for revision in revisions:
    # Un StyleDefinitionChange affecte strictement les styles et non les nœuds du document. Cela signifie que la propriété "ParentStyle" sera toujours utilisée, tandis que le ParentNode sera toujours nul.
    # Puisque toutes les autres modifications affectent les nœuds, le ParentNode sera inversement utilisé, et le ParentStyle sera nul.
    if revision.revision_type == aw.RevisionType.STYLE_DEFINITION_CHANGE:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, style: [{revision.parent_style.name}]')
    else:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, contents: [{revision.parent_node.get_text().strip()}]')
# Rejetez toutes les révisions via la collection, rétablissant le document à sa forme originale.
revisions.reject_all()
self.assertEqual(0, sum((1 for _ in revisions)))
```

### See Also

* module [aspose.words](../../)
* class [RevisionCollection](../)

