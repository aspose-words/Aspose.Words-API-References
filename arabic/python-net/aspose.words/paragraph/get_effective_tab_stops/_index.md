---
title: Paragraph.get_effective_tab_stops method
linktitle: get_effective_tab_stops method
articleTitle: get_effective_tab_stops method
second_title: Aspose.Words for Python
description: "Paragraph.get_effective_tab_stops method. Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists."
type: docs
weight: 270
url: /ar/python-net/aspose.words/paragraph/get_effective_tab_stops/
---

## get_effective_tab_stops() {#default}

Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists.


```python
def get_effective_tab_stops(self):
    ...
```

### Examples

Shows how to set custom tab stops for a paragraph.

```python
doc = aw.Document()
para = doc.first_section.body.first_paragraph
# إذا كنا في فقرة لا تحتوي على نقاط تبويب في هذه المجموعة،
# سيتقافز المؤشر 36 نقطة في كل مرة نضغط فيها مفتاح Tab في Microsoft Word.
self.assertEqual(0, len(doc.first_section.body.first_paragraph.get_effective_tab_stops()))
# يمكننا إضافة نقاط تبويب مخصصة في Microsoft Word إذا فعلنا المسطرة عبر علامة تبويب "View".
# كل وحدة على هذه المسطرة تمثل نقطتي تبويب افتراضيتين، أي 72 نقطة.
# يمكننا إضافة نقاط تبويب مخصصة برمجياً بهذه الطريقة.
tab_stops = doc.first_section.body.first_paragraph.paragraph_format.tab_stops
tab_stops.add(position=72, alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DOTS)
tab_stops.add(position=216, alignment=aw.TabAlignment.CENTER, leader=aw.TabLeader.DASHES)
tab_stops.add(position=360, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.LINE)
# يمكننا رؤية نقاط التبويب هذه في Microsoft Word عبر تفعيل المسطرة عبر "View" -> "Show" -> "Ruler".
self.assertEqual(3, len(para.get_effective_tab_stops()))
# أي أحرف تبويب نضيفها ستستخدم نقاط التبويب على المسطرة وقد،
# اعتماداً على قيمة القائد (tab leader)، تترك خطاً بين نقطة الانطلاق والوجهة.
para.append_child(aw.Run(doc=doc, text='\tTab 1\tTab 2\tTab 3'))
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.TabStops.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

