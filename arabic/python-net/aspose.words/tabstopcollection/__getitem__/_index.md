---
title: TabStopCollection indexer
linktitle: TabStopCollection indexer
articleTitle: TabStopCollection indexer
second_title: Aspose.Words for Python
description: "TabStopCollection indexer. Gets a tab stop at the given index."
type: docs
weight: 10
url: /ar/python-net/aspose.words/tabstopcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets a tab stop at the given index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to work with a document's collection of tab stops.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
tab_stops = builder.paragraph_format.tab_stops
# 72 نقطة تعادل "بوصة" واحدة على مسطرة إيقاف التبويب في Microsoft Word.
tab_stops.add(tab_stop=aw.TabStop(position=72))
tab_stops.add(tab_stop=aw.TabStop(position=432, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.DASHES))
self.assertEqual(2, tab_stops.count)
self.assertFalse(tab_stops[0].is_clear)
self.assertFalse(tab_stops[0].equals(tab_stops[1]))
# كل حرف "تبويب" ينقل مؤشر المُنشئ إلى موقع إيقاف التبويب التالي.
builder.writeln('Start\tTab 1\tTab 2')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(2, paragraphs.count)
# كل فقرة تحصل على مجموعة إيقافات التبويب الخاصة بها، التي تستنسخ قيمها من مجموعة إيقافات التبويب الخاصة بمُنشئ المستند.
self.assertEqual(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)
# يمكن لمجموعة إيقافات التبويب أن توجهنا إلى إيقافات التبويب قبل وبعد مواقع معينة.
self.assertEqual(72, tab_stops.before(100).position)
self.assertEqual(432, tab_stops.after(100).position)
# يمكننا مسح مجموعة إيقافات التبويب للفقرة للعودة إلى سلوك التبويب الافتراضي.
paragraphs[1].paragraph_format.tab_stops.clear()
self.assertEqual(0, paragraphs[1].paragraph_format.tab_stops.count)
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.TabStopCollection.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

