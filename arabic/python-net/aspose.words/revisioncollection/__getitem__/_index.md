---
title: RevisionCollection indexer
linktitle: RevisionCollection indexer
articleTitle: RevisionCollection indexer
second_title: Aspose.Words for Python
description: "RevisionCollection indexer. Returns a [Revision](../../revision/) at the specified index."
type: docs
weight: 10
url: /ar/python-net/aspose.words/revisioncollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Returns a [Revision](../../revision/) at the specified index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows how to work with revisions in a document.

```python
class ExRevision(ApiExampleBase):

    def test_revisions(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # التحرير العادي للمستند لا يُحتسب كمراجعة.
        builder.write('This does not count as a revision. ')
        self.assertFalse(doc.has_revisions)
        # لتسجيل تعديلاتنا كمراجعات، نحتاج إلى إعلان مؤلف، ثم بدء تتبعها.
        doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
        builder.write('This is revision #1. ')
        self.assertTrue(doc.has_revisions)
        self.assertEqual(1, doc.revisions.count)
        # هذه العلامة تتطابق مع خيار "مراجعة" -> "تتبع" -> "تتبع التغييرات" في Microsoft Word.
        # طريقة "StartTrackRevisions" لا تؤثر على قيمتها،
        # والمستند يتتبع المراجعات برمجيًا رغم أن قيمتها "false".
        # إذا فتحنا هذا المستند باستخدام Microsoft Word، فلن يتتبع المراجعات.
        self.assertFalse(doc.track_revisions)
        # لقد أضفنا نصًا باستخدام مُنشئ المستند، لذا فإن المراجعة الأولى هي مراجعة من نوع الإدراج.
        revision = doc.revisions[0]
        self.assertEqual('John Doe', revision.author)
        self.assertEqual('This is revision #1. ', revision.parent_node.get_text())
        self.assertEqual(aw.RevisionType.INSERTION, revision.revision_type)
        self.assertEqual(revision.date_time.date(), datetime.datetime.now().date())
        self.assertEqual(doc.revisions.groups[0], revision.group)
        # أزل تشغيلًا لإنشاء مراجعة من نوع الحذف.
        doc.first_section.body.first_paragraph.runs[0].remove()
        # إضافة مراجعة جديدة تضعها في بداية مجموعة المراجعات.
        self.assertEqual(aw.RevisionType.DELETION, doc.revisions[0].revision_type)
        self.assertEqual(2, doc.revisions.count)
        # تظهر مراجعات الإدراج في جسم المستند حتى قبل أن نقبل/نرفض المراجعة.
        # رفض المراجعة سيزيل العقد الخاصة بها من النص. وعلى العكس، العقد التي تشكل مراجعات الحذف
        # تستمر أيضًا في الوثيقة حتى نقبل المراجعة.
        self.assertEqual('This does not count as a revision. This is revision #1.', doc.get_text().strip())
        # قبول مراجعة الحذف سيزيل العقدة الأصلية من نص الفقرة
        # ثم يزيل مراجعة المجموعة نفسها.
        doc.revisions[0].accept()
        self.assertEqual(1, doc.revisions.count)
        self.assertEqual('This is revision #1.', doc.get_text().strip())
        builder.writeln('')
        builder.write('This is revision #2.')
        # الآن انقل العقدة لإنشاء نوع مراجعة متحركة.
        node = doc.first_section.body.paragraphs[1]
        end_node = doc.first_section.body.paragraphs[1].next_sibling
        reference_node = doc.first_section.body.paragraphs[0]
        while node != end_node:
            next_node = node.next_sibling
            doc.first_section.body.insert_before(node, reference_node)
            node = next_node
        self.assertEqual(aw.RevisionType.MOVING, doc.revisions[0].revision_type)
        self.assertEqual(8, doc.revisions.count)
        self.assertEqual('This is revision #2.\rThis is revision #1. \rThis is revision #2.', doc.get_text().strip())
        # المراجعة المتحركة الآن في الفهرس 1. رفض المراجعة لتجاهل محتوياتها.
        doc.revisions[1].reject()
        self.assertEqual(6, doc.revisions.count)
        self.assertEqual('This is revision #1. \rThis is revision #2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [RevisionCollection](../)

