---
title: Revision.parent_style property
linktitle: parent_style property
articleTitle: parent_style property
second_title: Aspose.Words for Python
description: "Revision.parent_style property. Gets the immediate parent style (owner) of this revision"
type: docs
weight: 50
url: /es/python-net/aspose.words/revision/parent_style/
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
# Esta colección en sí misma tiene una colección de grupos de revisiones.
# Cada grupo es una secuencia de revisiones adyacentes.
group_count = sum((1 for _ in revisions.groups))
print(f'{group_count} revision groups:')
# Itere sobre la colección de grupos e imprima el texto al que se refiere la revisión.
for group in revisions.groups:
    print(f'\tGroup type "{group.revision_type}", ' + f'author: {group.author}, contents: [{group.text.strip()}]')
# Cada Run que una revisión afecta obtiene un objeto Revision correspondiente.
# La colección de revisiones es considerablemente mayor que la forma condensada que imprimimos arriba,
# dependiendo de cuántos Runs hayamos segmentado el documento durante la edición en Microsoft Word.
revision_count = sum((1 for _ in revisions))
print(f'\n{revision_count} revisions:')
for revision in revisions:
    # Un StyleDefinitionChange afecta estrictamente a los estilos y no a los nodos del documento. Esto significa que la propiedad "ParentStyle" siempre estará en uso, mientras que ParentNode siempre será nulo.
    # Dado que todos los demás cambios afectan a los nodos, ParentNode estará en uso, y ParentStyle será nulo.
    if revision.revision_type == aw.RevisionType.STYLE_DEFINITION_CHANGE:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, style: [{revision.parent_style.name}]')
    else:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, contents: [{revision.parent_node.get_text().strip()}]')
# Rechace todas las revisiones mediante la colección, devolviendo el documento a su forma original.
revisions.reject_all()
self.assertEqual(0, sum((1 for _ in revisions)))
```

### See Also

* module [aspose.words](../../)
* class [Revision](../)

