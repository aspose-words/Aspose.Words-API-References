---
title: Revision.parent_style property
linktitle: parent_style property
articleTitle: parent_style property
second_title: Aspose.Words for Python
description: "Revision.parent_style property. Gets the immediate parent style (owner) of this revision"
type: docs
weight: 50
url: /ru/python-net/aspose.words/revision/parent_style/
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
# Эта коллекция сама содержит коллекцию групп исправлений.
# Каждая группа представляет собой последовательность смежных исправлений.
group_count = sum((1 for _ in revisions.groups))
print(f'{group_count} revision groups:')
# Итерируйте по коллекции групп и выводите текст, к которому относится исправление.
for group in revisions.groups:
    print(f'\tGroup type "{group.revision_type}", ' + f'author: {group.author}, contents: [{group.text.strip()}]')
# Каждый Run, на который влияет исправление, получает соответствующий объект Revision.
# Коллекция исправлений значительно больше, чем сокращённая форма, которую мы вывели выше,
# в зависимости от того, на сколько Run'ов мы разбили документ во время редактирования в Microsoft Word.
revision_count = sum((1 for _ in revisions))
print(f'\n{revision_count} revisions:')
for revision in revisions:
    # StyleDefinitionChange строго влияет на стили, а не на узлы документа. Это означает, что свойство "ParentStyle" всегда будет использоваться, тогда как ParentNode всегда будет null.
    # Поскольку все остальные изменения влияют на узлы, наоборот, будет использоваться ParentNode, а ParentStyle будет null.
    if revision.revision_type == aw.RevisionType.STYLE_DEFINITION_CHANGE:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, style: [{revision.parent_style.name}]')
    else:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, contents: [{revision.parent_node.get_text().strip()}]')
# Отклоните все исправления через коллекцию, вернув документ к его исходной форме.
revisions.reject_all()
self.assertEqual(0, sum((1 for _ in revisions)))
```

### See Also

* module [aspose.words](../../)
* class [Revision](../)

