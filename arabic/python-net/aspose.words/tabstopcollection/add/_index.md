---
title: TabStopCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.TabStopCollection.add method"
type: docs
weight: 30
url: /ar/python-net/aspose.words/tabstopcollection/add/
---

## add(tab_stop) {#tabstop}

Adds or replaces a tab stop in the collection.


```python
def add(self, tab_stop: aspose.words.TabStop):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| tab_stop | [TabStop](../../tabstop/) | A tab stop object to add. |

### Remarks

If a tab stop already exists at the specified position, it is replaced.




## add(position, alignment, leader) {#float_tabalignment_tableader}

Adds or replaces a tab stop in the collection.


```python
def add(self, position: float, alignment: aspose.words.TabAlignment, leader: aspose.words.TabLeader):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | float | A position (in points) where to add the tab stop. |
| alignment | [TabAlignment](../../tabalignment/) | A [TabAlignment](../../tabalignment/) value that specifies the alignment of text at the tab stop. |
| leader | [TabLeader](../../tableader/) | A [TabLeader](../../tableader/) value that specifies the type of the leader line displayed under the tab character. |

### Remarks

If a tab stop already exists at the specified position, it is replaced.




## Examples

Shows how to add custom tab stops to a document.

```python
doc = aw.Document()
paragraph = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# فيما يلي طريقتان لإضافة نقاط تبويب إلى مجموعة نقاط تبويب الفقرة عبر خاصية "ParagraphFormat".
# 1 -  أنشئ كائن "TabStop"، ثم أضفه إلى المجموعة:
tab_stop = aw.TabStop(position=aw.ConvertUtil.inch_to_point(3), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
paragraph.paragraph_format.tab_stops.add(tab_stop=tab_stop)
# 2 -  مرّر القيم لخصائص نقطة تبويب جديدة إلى طريقة "Add":
paragraph.paragraph_format.tab_stops.add(position=aw.ConvertUtil.millimeter_to_point(100), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
# أضف نقاط تبويب على بعد 5 سم إلى جميع الفقرات.
for para in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)))):
    para.paragraph_format.tab_stops.add(position=aw.ConvertUtil.millimeter_to_point(50), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
# كل حرف "تبويب" ينقل مؤشر المُنشئ إلى موقع إيقاف التبويب التالي.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Start\tTab 1\tTab 2\tTab 3\tTab 4')
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.AddTabStops.docx')
```

## See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

