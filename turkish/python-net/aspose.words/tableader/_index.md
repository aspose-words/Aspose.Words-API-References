---
title: TabLeader enumeration
linktitle: TabLeader enumeration
articleTitle: TabLeader enumeration
second_title: Aspose.Words for Python
description: "aspose.words.TabLeader enumeration. Specifies the type of the leader line displayed under the tab character."
type: docs
weight: 1290
url: /tr/python-net/aspose.words/tableader/
---

## TabLeader enumeration

Specifies the type of the leader line displayed under the tab character.


### Members

| Name | Description |
| --- | --- |
| NONE | No leader line is displayed. |
| DOTS | The leader line is made up from dots. |
| DASHES | The leader line is made up from dashes. |
| LINE | The leader line is a single line. |
| HEAVY | The leader line is a single thick line. |
| MIDDLE_DOT | The leader line is made up from middle-dots. |

### Examples

Shows how to set custom tab stops for a paragraph.

```python
doc = aw.Document()
para = doc.first_section.body.first_paragraph
# Bu koleksiyonda sekme durakları olmayan bir paragrafta isek,
# imleç, Microsoft Word'de Tab tuşuna her bastığımızda 36 puan atlayacaktır.
self.assertEqual(0, len(doc.first_section.body.first_paragraph.get_effective_tab_stops()))
# Microsoft Word'de cetveli "View" sekmesi aracılığıyla etkinleştirirsek özel sekme durakları ekleyebiliriz.
# Bu cetveldeki her birim iki varsayılan sekme durakıdır ve 72 puana eşittir.
# Özel sekme duraklarını programlı olarak şu şekilde ekleyebiliriz.
tab_stops = doc.first_section.body.first_paragraph.paragraph_format.tab_stops
tab_stops.add(position=72, alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DOTS)
tab_stops.add(position=216, alignment=aw.TabAlignment.CENTER, leader=aw.TabLeader.DASHES)
tab_stops.add(position=360, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.LINE)
# Bu sekme duraklarını, "View" -> "Show" -> "Ruler" yoluyla cetveli etkinleştirerek Microsoft Word'de görebiliriz.
self.assertEqual(3, len(para.get_effective_tab_stops()))
# Eklediğimiz herhangi bir sekme karakteri, cetveldeki sekme duraklarını kullanacak ve olabilir,
# sekme liderinin değerine bağlı olarak, sekme başlangıcı ile varış noktası arasında bir çizgi bırakabilir.
para.append_child(aw.Run(doc=doc, text='\tTab 1\tTab 2\tTab 3'))
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.TabStops.docx')
```

### See Also

* module [aspose.words](../)

