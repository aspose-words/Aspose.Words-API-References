---
title: TabStopCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "TabStopCollection.clear method. Deletes all tab stop positions."
type: docs
weight: 60
url: /ru/python-net/aspose.words/tabstopcollection/clear/
---

## clear() {#default}

Deletes all tab stop positions.


```python
def clear(self):
    ...
```

### Examples

Shows how to work with a document's collection of tab stops.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
tab_stops = builder.paragraph_format.tab_stops
# 72 пункта — это один \"дюйм\" на линейке табуляции Microsoft Word.
tab_stops.add(tab_stop=aw.TabStop(position=72))
tab_stops.add(tab_stop=aw.TabStop(position=432, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.DASHES))
self.assertEqual(2, tab_stops.count)
self.assertFalse(tab_stops[0].is_clear)
self.assertFalse(tab_stops[0].equals(tab_stops[1]))
# Каждый символ \"tab\" перемещает курсор построителя к позиции следующей табуляции.
builder.writeln('Start\tTab 1\tTab 2')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(2, paragraphs.count)
# Каждый абзац получает свою коллекцию табуляций, которая клонирует значения из коллекции табуляций построителя документа.
self.assertEqual(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)
# Коллекция табуляций может указывать нам на TabStops до и после определённых позиций.
self.assertEqual(72, tab_stops.before(100).position)
self.assertEqual(432, tab_stops.after(100).position)
# Мы можем очистить коллекцию табуляций абзаца, чтобы вернуть поведение табуляции по умолчанию.
paragraphs[1].paragraph_format.tab_stops.clear()
self.assertEqual(0, paragraphs[1].paragraph_format.tab_stops.count)
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.TabStopCollection.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

