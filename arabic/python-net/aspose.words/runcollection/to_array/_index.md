---
title: RunCollection.to_array method
linktitle: to_array method
articleTitle: to_array method
second_title: Aspose.Words for Python
description: "RunCollection.to_array method. Copies all runs from the collection to a new array of runs."
type: docs
weight: 20
url: /ar/python-net/aspose.words/runcollection/to_array/
---

## to_array() {#default}

Copies all runs from the collection to a new array of runs.


```python
def to_array(self):
    ...
```

### Returns

An array of runs.


### Examples

Shows how to determine the revision type of an inline node.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision runs.docx')
# عند تحرير المستند بينما يكون خيار "Track Changes" مفعلًا، الموجود عبر مراجعة -> تتبع،
# يتم تشغيله في Microsoft Word، وتُحسب التغييرات التي نُجريها كمراجعات.
# عند تحرير مستند باستخدام Aspose.Words، يمكننا بدء تتبع المراجعات عن طريق
# استدعاء طريقة "StartTrackRevisions" للمستند وإيقاف التتبع باستخدام طريقة "StopTrackRevisions".
# يمكننا إما قبول المراجعات لدمجها في المستند
# أو رفضها لتغيير التعديل المقترح بفعالية.
self.assertEqual(6, doc.revisions.count)
# العقدة الأصلية للمراجعة هي الـ Run الذي تتعلق به المراجعة. الـ Run هو عقدة Inline.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# فيما يلي خمسة أنواع من المراجعات التي يمكن أن تضع علامة على عقدة Inline.
# 1 -  مراجعة "insert":
# تحدث هذه المراجعة عندما نقوم بإدراج نص أثناء تتبع التغييرات.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  مراجعة "format":
# تحدث هذه المراجعة عندما نغير تنسيق النص أثناء تتبع التغييرات.
self.assertTrue(runs[2].is_format_revision)
# 3 -  مراجعة "move from":
# عندما نحدد نصًا في Microsoft Word، ثم نسحبه إلى مكان مختلف في المستند
# أثناء تتبع التغييرات، تظهر مراجعتان.
# مراجعة "move from" هي نسخة من النص الأصلي قبل أن نقوم بنقله.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  مراجعة "move to":
# مراجعة "move to" هي النص الذي نقلناه إلى موقعه الجديد في المستند.
# مراجعات "Move from" و "move to" تظهر في أزواج لكل عملية نقل نقوم بها.
# قبول مراجعة النقل يحذف مراجعة "move from" والنص الخاص بها،
# ويحتفظ بالنص من مراجعة "move to".
# رفض مراجعة النقل على العكس يحتفظ بمراجعة "move from" ويحذف مراجعة "move to".
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  مراجعة "delete":
# تحدث هذه المراجعة عندما نحذف نصًا أثناء تتبع التغييرات. عندما نحذف النص بهذه الطريقة،
# سيبقى في المستند كمراجعة حتى نقبل المراجعة،
# والتي ستحذف النص نهائيًا، أو ترفض المراجعة، والتي ستحافظ على النص الذي حذفناه في مكانه.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [RunCollection](../)

