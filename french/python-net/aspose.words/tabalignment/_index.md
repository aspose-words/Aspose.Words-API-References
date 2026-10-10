---
title: TabAlignment enumeration
linktitle: TabAlignment enumeration
articleTitle: TabAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.TabAlignment enumeration. Specifies the alignment/type of a tab stop."
type: docs
weight: 1280
url: /fr/python-net/aspose.words/tabalignment/
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
# Si nous sommes dans un paragraphe sans tabulations dans cette collection,
# le curseur sautera de 36 points chaque fois que nous appuyons sur la touche Tab dans Microsoft Word.
self.assertEqual(0, len(doc.first_section.body.first_paragraph.get_effective_tab_stops()))
# Nous pouvons ajouter des tabulations personnalisées dans Microsoft Word si nous activons la règle via l'onglet "View".
# Chaque unité de cette règle correspond à deux tabulations par défaut, soit 72 points.
# Nous pouvons ajouter des tabulations personnalisées programmatiquement ainsi.
tab_stops = doc.first_section.body.first_paragraph.paragraph_format.tab_stops
tab_stops.add(position=72, alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DOTS)
tab_stops.add(position=216, alignment=aw.TabAlignment.CENTER, leader=aw.TabLeader.DASHES)
tab_stops.add(position=360, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.LINE)
# Nous pouvons voir ces tabulations dans Microsoft Word en activant la règle via "View" -> "Show" -> "Ruler".
self.assertEqual(3, len(para.get_effective_tab_stops()))
# Tout caractère de tabulation que nous ajoutons utilisera les tabulations de la règle et pourra,
# en fonction de la valeur du leader de tabulation, laisser une ligne entre les points de départ et d'arrivée de la tabulation.
para.append_child(aw.Run(doc=doc, text='\tTab 1\tTab 2\tTab 3'))
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.TabStops.docx')
```

### See Also

* module [aspose.words](../)

