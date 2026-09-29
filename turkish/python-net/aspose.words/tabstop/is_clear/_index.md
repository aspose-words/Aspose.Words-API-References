---
title: TabStop.is_clear property
linktitle: is_clear property
articleTitle: is_clear property
second_title: Aspose.Words for Python
description: "TabStop.is_clear property. Returns ``True`` if this tab stop clears any existing tab stops in this position."
type: docs
weight: 30
url: /tr/python-net/aspose.words/tabstop/is_clear/
---

## TabStop.is_clear property

Returns ``True`` if this tab stop clears any existing tab stops in this position.



```python
@property
def is_clear(self) -> bool:
    ...

```

### Examples

Shows how to work with a document's collection of tab stops.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
tab_stops = builder.paragraph_format.tab_stops
# 72 puan, Microsoft Word sekme durağı cetvelinde bir \"inç\"e eşittir.
tab_stops.add(tab_stop=aw.TabStop(position=72))
tab_stops.add(tab_stop=aw.TabStop(position=432, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.DASHES))
self.assertEqual(2, tab_stops.count)
self.assertFalse(tab_stops[0].is_clear)
self.assertFalse(tab_stops[0].equals(tab_stops[1]))
# Her \"tab\" karakteri, oluşturucunun imlecini bir sonraki sekme durağının konumuna götürür.
builder.writeln('Start\tTab 1\tTab 2')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(2, paragraphs.count)
# Her paragraf, değerlerini belge oluşturucusunun sekme durağı koleksiyonundan kopyalayan kendi sekme durağı koleksiyonunu alır.
self.assertEqual(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)
# Bir sekme durağı koleksiyonu, belirli konumların öncesi ve sonrasındaki TabStop'lara işaret edebilir.
self.assertEqual(72, tab_stops.before(100).position)
self.assertEqual(432, tab_stops.after(100).position)
# Varsayılan sekme davranışına dönmek için bir paragrafın sekme durağı koleksiyonunu temizleyebiliriz.
paragraphs[1].paragraph_format.tab_stops.clear()
self.assertEqual(0, paragraphs[1].paragraph_format.tab_stops.count)
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.TabStopCollection.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStop](../)

