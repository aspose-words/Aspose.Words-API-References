---
title: RevisionCollection.groups property
linktitle: groups property
articleTitle: groups property
second_title: Aspose.Words for Python
description: "RevisionCollection.groups property. Collection of revision groups."
type: docs
weight: 30
url: /it/python-net/aspose.words/revisioncollection/groups/
---

## RevisionCollection.groups property

Collection of revision groups.


```python
@property
def groups(self) -> aspose.words.RevisionGroupCollection:
    ...

```

### Examples

Shows how to work with a document's collection of revisions.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
revisions = doc.revisions
# Questa collezione stessa contiene una collezione di gruppi di revisione.
# Ogni gruppo è una sequenza di revisioni adiacenti.
group_count = sum((1 for _ in revisions.groups))
print(f'{group_count} revision groups:')
# Itera sulla collezione di gruppi e stampa il testo a cui la revisione si riferisce.
for group in revisions.groups:
    print(f'\tGroup type "{group.revision_type}", ' + f'author: {group.author}, contents: [{group.text.strip()}]')
# Ogni Run che una revisione colpisce ottiene un oggetto Revision corrispondente.
# La collezione delle revisioni è considerevolmente più grande della forma condensata che abbiamo stampato sopra,
# a seconda di quante Run abbiamo segmentato il documento durante la modifica con Microsoft Word.
revision_count = sum((1 for _ in revisions))
print(f'\n{revision_count} revisions:')
for revision in revisions:
    # Uno StyleDefinitionChange influisce strettamente sugli stili e non sui nodi del documento. Questo significa che la proprietà "ParentStyle" sarà sempre in uso, mentre ParentNode sarà sempre null.
    # Poiché tutte le altre modifiche influenzano i nodi, ParentNode sarà al contrario in uso, e ParentStyle sarà null.
    if revision.revision_type == aw.RevisionType.STYLE_DEFINITION_CHANGE:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, style: [{revision.parent_style.name}]')
    else:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, contents: [{revision.parent_node.get_text().strip()}]')
# Rifiuta tutte le revisioni tramite la collezione, ripristinando il documento alla sua forma originale.
revisions.reject_all()
self.assertEqual(0, sum((1 for _ in revisions)))
```

### See Also

* module [aspose.words](../../)
* class [RevisionCollection](../)

