---
title: TabStopCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.TabStopCollection.add method"
type: docs
weight: 30
url: /de/python-net/aspose.words/tabstopcollection/add/
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
# Unten sind zwei Methoden zum Hinzufügen von Tabstopps zur Tabstopp-Sammlung eines Absatzes über die "ParagraphFormat"-Eigenschaft aufgeführt.
# 1 -  Erstellen Sie ein "TabStop"-Objekt und fügen Sie es anschließend zur Sammlung hinzu:
tab_stop = aw.TabStop(position=aw.ConvertUtil.inch_to_point(3), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
paragraph.paragraph_format.tab_stops.add(tab_stop=tab_stop)
# 2 -  Übergeben Sie die Werte für die Eigenschaften eines neuen Tabstopps an die "Add"-Methode:
paragraph.paragraph_format.tab_stops.add(position=aw.ConvertUtil.millimeter_to_point(100), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
# Fügen Sie allen Absätzen Tabstopps bei 5 cm hinzu.
for para in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)))):
    para.paragraph_format.tab_stops.add(position=aw.ConvertUtil.millimeter_to_point(50), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
# Jedes \"Tab\"-Zeichen bewegt den Cursor des Builders zur Position des nächsten Tabstopp.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Start\tTab 1\tTab 2\tTab 3\tTab 4')
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.AddTabStops.docx')
```

## See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

