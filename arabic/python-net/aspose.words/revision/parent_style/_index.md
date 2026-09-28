---
title: Revision.parent_style property
linktitle: parent_style property
articleTitle: parent_style property
second_title: Aspose.Words for Python
description: "Revision.parent_style property. Gets the immediate parent style (owner) of this revision"
type: docs
weight: 50
url: /ar/python-net/aspose.words/revision/parent_style/
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
# هذه المجموعة نفسها تحتوي على مجموعة من مجموعات المراجعات.
# كل مجموعة هي تسلسل من المراجعات المتجاورة.
group_count = sum((1 for _ in revisions.groups))
print(f'{group_count} revision groups:')
# تكرّر عبر مجموعة المجموعات واطبع النص الذي تتعلق به المراجعة.
for group in revisions.groups:
    print(f'\tGroup type "{group.revision_type}", ' + f'author: {group.author}, contents: [{group.text.strip()}]')
# كل Run تتأثر به مراجعة يحصل على كائن Revision المقابل.
# مجموعة المراجعات أكبر بكثير من الشكل المختصر الذي طبعناه أعلاه،
# اعتماداً على عدد الـ Runs التي قسمنا المستند إليها أثناء تحرير Microsoft Word.
revision_count = sum((1 for _ in revisions))
print(f'\n{revision_count} revisions:')
for revision in revisions:
    # تؤثر StyleDefinitionChange بشكل صارم على الأنماط وليس على عقد المستند. هذا يعني أن الخاصية "ParentStyle" ستكون دائماً قيد الاستخدام، بينما سيكون ParentNode دائماً null.
    # نظرًا لأن جميع التغييرات الأخرى تؤثر على العقد، سيكون ParentNode عكس ذلك قيد الاستخدام، وستكون ParentStyle null.
    if revision.revision_type == aw.RevisionType.STYLE_DEFINITION_CHANGE:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, style: [{revision.parent_style.name}]')
    else:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, contents: [{revision.parent_node.get_text().strip()}]')
# ارفض جميع المراجعات عبر المجموعة، مع إرجاع المستند إلى شكله الأصلي.
revisions.reject_all()
self.assertEqual(0, sum((1 for _ in revisions)))
```

### See Also

* module [aspose.words](../../)
* class [Revision](../)

