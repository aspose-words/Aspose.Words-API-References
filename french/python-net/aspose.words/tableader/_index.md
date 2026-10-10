---
title: TabLeader enumeration
linktitle: TabLeader enumeration
articleTitle: TabLeader enumeration
second_title: Aspose.Words for Python
description: "aspose.words.TabLeader enumeration. Specifies the type of the leader line displayed under the tab character."
type: docs
weight: 1290
url: /fr/python-net/aspose.words/tableader/
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

