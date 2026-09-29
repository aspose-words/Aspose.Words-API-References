---
title: Revision.parent_style property
linktitle: parent_style property
articleTitle: parent_style property
second_title: Aspose.Words for Python
description: "Revision.parent_style property. Gets the immediate parent style (owner) of this revision"
type: docs
weight: 50
url: /sv/python-net/aspose.words/revision/parent_style/
---

## Revision.parent_style property

Gets the immediate parent style (owner) of this revision.
This property will work for only for the [RevisionType.STYLE_DEFINITION_CHANGE](../../revisiontype/#STYLE_DEFINITION_CHANGE) revision type.



```python
@property
def parent_style(self) -> aspose.words.Style:
    ...

```

### Remarks

If this revision relates to changes on document nodes, use [Revision.parent_node](../parent_node/) instead.



### Examples

Shows how to work with a document's collection of revisions.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
revisions = doc.revisions
# Den här samlingen har i sig en samling av revisionsgrupper.
# Varje grupp är en sekvens av intilliggande revisioner.
group_count = sum((1 for _ in revisions.groups))
print(f'{group_count} revision groups:')
# Iterera över samlingen av grupper och skriv ut den text som revisionen gäller.
for group in revisions.groups:
    print(f'\tGroup type "{group.revision_type}", ' + f'author: {group.author}, contents: [{group.text.strip()}]')
# Varje Run som en revision påverkar får ett motsvarande Revision-objekt.
# Revisionernas samling är avsevärt större än den kondenserade formen vi skrev ut ovan,
# beroende på hur många Run vi har segmenterat dokumentet i under Microsoft Word-redigering.
revision_count = sum((1 for _ in revisions))
print(f'\n{revision_count} revisions:')
for revision in revisions:
    # En StyleDefinitionChange påverkar strikt stilar och inte dokumentnoder. Detta betyder att egenskapen "ParentStyle" alltid kommer att vara i bruk, medan ParentNode alltid kommer att vara null.
    # Eftersom alla andra ändringar påverkar noder, kommer ParentNode i motsats till detta att vara i bruk, och ParentStyle blir null.
    if revision.revision_type == aw.RevisionType.STYLE_DEFINITION_CHANGE:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, style: [{revision.parent_style.name}]')
    else:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, contents: [{revision.parent_node.get_text().strip()}]')
# Avvisa alla revisioner via samlingen, så att dokumentet återgår till sin ursprungliga form.
revisions.reject_all()
self.assertEqual(0, sum((1 for _ in revisions)))
```

### See Also

* module [aspose.words](../../)
* class [Revision](../)

