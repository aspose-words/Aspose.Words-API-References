---
title: RevisionCollection.reject_all method
linktitle: reject_all method
articleTitle: reject_all method
second_title: Aspose.Words for Python
description: "RevisionCollection.reject_all method. Rejects all revisions in this collection."
type: docs
weight: 70
url: /de/python-net/aspose.words/revisioncollection/reject_all/
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
# Diese Sammlung enthält selbst eine Sammlung von Revisionsgruppen.
# Jede Gruppe ist eine Sequenz benachbarter Revisionen.
group_count = sum((1 for _ in revisions.groups))
print(f'{group_count} revision groups:')
# Iterieren Sie über die Sammlung von Gruppen und geben Sie den Text aus, den die Revision betrifft.
for group in revisions.groups:
    print(f'\tGroup type "{group.revision_type}", ' + f'author: {group.author}, contents: [{group.text.strip()}]')
# Jeder Run, den eine Revision betrifft, erhält ein entsprechendes Revision-Objekt.
# Die Revisionensammlung ist deutlich größer als die komprimierte Form, die wir oben ausgegeben haben,
# abhängig davon, in wie viele Runs wir das Dokument während der Microsoft‑Word‑Bearbeitung segmentiert haben.
revision_count = sum((1 for _ in revisions))
print(f'\n{revision_count} revisions:')
for revision in revisions:
    # Ein StyleDefinitionChange wirkt sich ausschließlich auf Stile und nicht auf Dokumentknoten aus. Das bedeutet, dass die Eigenschaft "ParentStyle" immer verwendet wird, während ParentNode immer null ist.
    # Da alle anderen Änderungen Knoten betreffen, wird ParentNode im Gegenzug verwendet und ParentStyle ist null.
    if revision.revision_type == aw.RevisionType.STYLE_DEFINITION_CHANGE:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, style: [{revision.parent_style.name}]')
    else:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, contents: [{revision.parent_node.get_text().strip()}]')
# Verwerfen Sie alle Revisionen über die Sammlung und stellen Sie das Dokument in seine ursprüngliche Form zurück.
revisions.reject_all()
self.assertEqual(0, sum((1 for _ in revisions)))
```

### See Also

* module [aspose.words](../../)
* class [RevisionCollection](../)

