---
title: RevisionCollection.groups property
linktitle: groups property
articleTitle: groups property
second_title: Aspose.Words for Python
description: "RevisionCollection.groups property. Collection of revision groups."
type: docs
weight: 30
url: /tr/python-net/aspose.words/revisioncollection/groups/
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
# Bu koleksiyonun kendisi bir revizyon grubu koleksiyonuna sahiptir.
# Her grup, yan yana gelen revizyonların bir dizisidir.
group_count = sum((1 for _ in revisions.groups))
print(f'{group_count} revision groups:')
# Grupların koleksiyonunu döngüyle gezerek revizyonun ilgili olduğu metni yazdırın.
for group in revisions.groups:
    print(f'\tGroup type "{group.revision_type}", ' + f'author: {group.author}, contents: [{group.text.strip()}]')
# Bir revizyonun etkilediği her Run, karşılık gelen bir Revision nesnesi alır.
# Revizyonların koleksiyonu, yukarıda yazdırdığımız sıkıştırılmış formdan oldukça daha büyüktür,
# Microsoft Word düzenlemesi sırasında belgeyi kaç Run'a bölüştürdüğümüze bağlı olarak.
revision_count = sum((1 for _ in revisions))
print(f'\n{revision_count} revisions:')
for revision in revisions:
    # Bir StyleDefinitionChange yalnızca stilleri etkiler ve belge düğümlerini etkilemez. Bu, "ParentStyle" özelliğinin her zaman kullanılacağı, ParentNode'un ise her zaman null olacağı anlamına gelir.
    # Diğer tüm değişiklikler düğümleri etkilediği için, ParentNode tersine kullanılacak ve ParentStyle null olacaktır.
    if revision.revision_type == aw.RevisionType.STYLE_DEFINITION_CHANGE:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, style: [{revision.parent_style.name}]')
    else:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, contents: [{revision.parent_node.get_text().strip()}]')
# Koleksiyon aracılığıyla tüm revizyonları reddederek belgeyi orijinal haline geri döndürün.
revisions.reject_all()
self.assertEqual(0, sum((1 for _ in revisions)))
```

### See Also

* module [aspose.words](../../)
* class [RevisionCollection](../)

