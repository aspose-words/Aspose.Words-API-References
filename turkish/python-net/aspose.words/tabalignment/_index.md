---
title: TabAlignment enumeration
linktitle: TabAlignment enumeration
articleTitle: TabAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.TabAlignment enumeration. Specifies the alignment/type of a tab stop."
type: docs
weight: 1280
url: /tr/python-net/aspose.words/tabalignment/
---

## TabAlignment enumeration

Specifies the alignment/type of a tab stop.


### Members

| Name | Description |
| --- | --- |
| LEFT | Left-aligns the text after the tab stop. |
| CENTER | Centers the text around the tab stop. |
| RIGHT | Right-aligns the text at the tab stop. |
| DECIMAL | Aligns the text at the decimal dot. |
| BAR | Draws a vertical bar at the tab stop position. |
| LIST | The tab is a delimiter between the number/bullet and text in a list item. |
| CLEAR | Clears any tab stop in this position. |

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

