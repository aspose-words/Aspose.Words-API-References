---
title: Paragraph.is_move_from_revision property
linktitle: is_move_from_revision property
articleTitle: is_move_from_revision property
second_title: Aspose.Words for Python
description: "Paragraph.is_move_from_revision property. Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 130
url: /ar/python-net/aspose.words/paragraph/is_move_from_revision/
---

## Paragraph.is_move_from_revision property

Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_from_revision(self) -> bool:
    ...

```

### Examples

Shows how to check whether a paragraph is a move revision.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# يحتوي هذا المستند على مراجعات \"Move\"، التي تظهر عندما نحدد النص بالمؤشر،
# ثم نسحبها لنقلها إلى موقع آخر
# أثناء تتبع المراجعات في Microsoft Word عبر \"Review\" -> \"Track changes\".
self.assertEqual(6, len(list(filter(lambda r: r.revision_type == aw.RevisionType.MOVING, doc.revisions))))
paragraphs = doc.first_section.body.paragraphs
# تتكون مراجعات Move من أزواج من مراجعات \"Move from\" و \"Move to\".
# هذه المراجعات هي تغييرات محتملة في المستند يمكننا إما قبولها أو رفضها.
# قبل أن نقبل/نرفض مراجعة النقل، المستند
# يجب أن يتتبع كلًا من وجهتي المغادرة والوصول للنص.
# الفقرة الثانية والرابعة تحددان مراجعة من هذا النوع، وبالتالي كلاهما يحتويان على نفس المحتوى.
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# مراجعة \"Move from\" هي الفقرة التي سحبنا النص منها.
# إذا قبلنا المراجعة، ستختفي هذه الفقرة،
# والأخرى ستبقى ولن تكون مراجعة بعد الآن.
self.assertTrue(paragraphs[1].is_move_from_revision)
# مراجعة \"Move to\" هي الفقرة التي سحبنا النص إليها.
# إذا رفضنا المراجعة، ستختفي هذه الفقرة بدلاً من ذلك، وستبقى الأخرى.
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

