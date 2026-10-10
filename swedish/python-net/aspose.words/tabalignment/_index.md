---
title: TabAlignment enumeration
linktitle: TabAlignment enumeration
articleTitle: TabAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.TabAlignment enumeration. Specifies the alignment/type of a tab stop."
type: docs
weight: 1280
url: /sv/python-net/aspose.words/tabalignment/
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

* module [aspose.words](../)

