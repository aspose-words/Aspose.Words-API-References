---
title: InlineStory.is_move_to_revision property
linktitle: is_move_to_revision property
articleTitle: is_move_to_revision property
second_title: Aspose.Words for Python
description: "InlineStory.is_move_to_revision property. Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 60
url: /ar/python-net/aspose.words/inlinestory/is_move_to_revision/
---

## InlineStory.is_move_to_revision property

Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_to_revision(self) -> bool:
    ...

```

### Examples

Shows how to view revision-related properties of InlineStory nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision footnotes.docx')
# عند تحرير المستند بينما يكون خيار "Track Changes" مفعلًا، الموجود عبر مراجعة -> تتبع،
# يتم تشغيله في Microsoft Word، وتُحسب التغييرات التي نُجريها كمراجعات.
# عند تحرير مستند باستخدام Aspose.Words، يمكننا بدء تتبع المراجعات عن طريق
# استدعاء طريقة "StartTrackRevisions" للمستند وإيقاف التتبع باستخدام طريقة "StopTrackRevisions".
# يمكننا إما قبول المراجعات لدمجها في المستند
# أو رفضها للتراجع وإلغاء التغيير المقترح.
self.assertTrue(doc.has_revisions)
footnotes = list(map(lambda x: x.as_footnote(), list(doc.get_child_nodes(aw.NodeType.FOOTNOTE, True))))
self.assertEqual(5, len(footnotes))
# فيما يلي خمسة أنواع من المراجعات التي يمكن أن تضع علامة على عقدة InlineStory.
# 1 -  مراجعة "insert":
# تحدث هذه المراجعة عندما نقوم بإدراج نص أثناء تتبع التغييرات.
self.assertTrue(footnotes[2].is_insert_revision)
# 2 -  مراجعة "move from":
# عندما نحدد نصًا في Microsoft Word، ثم نسحبه إلى مكان مختلف في المستند
# أثناء تتبع التغييرات، تظهر مراجعتان.
# مراجعة "move from" هي نسخة من النص الأصلي قبل أن نقوم بنقله.
self.assertTrue(footnotes[4].is_move_from_revision)
# 3 -  مراجعة "move to":
# مراجعة "move to" هي النص الذي نقلناه إلى موقعه الجديد في المستند.
# مراجعات "Move from" و "move to" تظهر في أزواج لكل عملية نقل نقوم بها.
# قبول مراجعة النقل يحذف مراجعة "move from" والنص الخاص بها،
# ويحتفظ بالنص من مراجعة "move to".
# رفض مراجعة النقل على العكس يحتفظ بمراجعة "move from" ويحذف مراجعة "move to".
self.assertTrue(footnotes[1].is_move_to_revision)
# 4 -  مراجعة "delete":
# تحدث هذه المراجعة عندما نحذف نصًا أثناء تتبع التغييرات. عندما نحذف النص بهذه الطريقة،
# سيبقى في المستند كمراجعة حتى نقبل المراجعة،
# والتي ستحذف النص نهائيًا، أو ترفض المراجعة، والتي ستحافظ على النص الذي حذفناه في مكانه.
self.assertTrue(footnotes[3].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

