---
title: Paragraph.get_effective_tab_stops method
linktitle: get_effective_tab_stops method
articleTitle: get_effective_tab_stops method
second_title: Aspose.Words for Python
description: "Paragraph.get_effective_tab_stops method. Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists."
type: docs
weight: 270
url: /sv/python-net/aspose.words/paragraph/get_effective_tab_stops/
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
# Om vi befinner oss i ett stycke utan tabbstopp i denna samling,
# kommer markören att hoppa 36 punkter varje gång vi trycker på Tab-tangenten i Microsoft Word.
self.assertEqual(0, len(doc.first_section.body.first_paragraph.get_effective_tab_stops()))
# Vi kan lägga till anpassade tabbstopp i Microsoft Word om vi aktiverar linjalen via fliken "View".
# Varje enhet på denna linjal motsvarar två standardtabbstopp, vilket är 72 punkter.
# Vi kan lägga till anpassade tabbstopp programmässigt på detta sätt.
tab_stops = doc.first_section.body.first_paragraph.paragraph_format.tab_stops
tab_stops.add(position=72, alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DOTS)
tab_stops.add(position=216, alignment=aw.TabAlignment.CENTER, leader=aw.TabLeader.DASHES)
tab_stops.add(position=360, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.LINE)
# Vi kan se dessa tabbstopp i Microsoft Word genom att aktivera linjalen via "View" -> "Show" -> "Ruler".
self.assertEqual(3, len(para.get_effective_tab_stops()))
# Alla tab-tecken vi lägger till kommer att använda tabbstoppen på linjalen och kan,
# beroende på tabbleaderns värde, lämna en linje mellan tabbens start- och ankomstpunkter.
para.append_child(aw.Run(doc=doc, text='\tTab 1\tTab 2\tTab 3'))
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.TabStops.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

