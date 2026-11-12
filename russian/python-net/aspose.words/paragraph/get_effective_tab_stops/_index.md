---
title: Paragraph.get_effective_tab_stops method
linktitle: get_effective_tab_stops method
articleTitle: get_effective_tab_stops method
second_title: Aspose.Words for Python
description: "Paragraph.get_effective_tab_stops method. Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists."
type: docs
weight: 270
url: /ru/python-net/aspose.words/paragraph/get_effective_tab_stops/
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
# Если мы находимся в абзаце без табуляций в этой коллекции,
# курсор будет перемещаться на 36 пунктов каждый раз, когда мы нажимаем клавишу Tab в Microsoft Word.
self.assertEqual(0, len(doc.first_section.body.first_paragraph.get_effective_tab_stops()))
# Мы можем добавить пользовательские табуляции в Microsoft Word, если включим линейку через вкладку "View".
# Каждая единица на этой линейке соответствует двум стандартным табуляциям, что составляет 72 пункта.
# Мы можем добавить пользовательские табуляции программно, как показано ниже.
tab_stops = doc.first_section.body.first_paragraph.paragraph_format.tab_stops
tab_stops.add(position=72, alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DOTS)
tab_stops.add(position=216, alignment=aw.TabAlignment.CENTER, leader=aw.TabLeader.DASHES)
tab_stops.add(position=360, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.LINE)
# Мы можем увидеть эти табуляции в Microsoft Word, включив линейку через "View" -> "Show" -> "Ruler".
self.assertEqual(3, len(para.get_effective_tab_stops()))
# Любые добавленные нами символы табуляции будут использовать табуляции на линейке и могут,
# в зависимости от значения табуляционного лидера, оставлять линию между началом и конечным пунктом табуляции.
para.append_child(aw.Run(doc=doc, text='\tTab 1\tTab 2\tTab 3'))
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.TabStops.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

