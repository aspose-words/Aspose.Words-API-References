---
title: Paragraph.get_effective_tab_stops method
linktitle: get_effective_tab_stops method
articleTitle: get_effective_tab_stops method
second_title: Aspose.Words for Python
description: "Paragraph.get_effective_tab_stops method. Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists."
type: docs
weight: 270
url: /de/python-net/aspose.words/paragraph/get_effective_tab_stops/
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
# Wenn wir uns in einem Absatz ohne Tabstopps in dieser Sammlung befinden,
# springt der Cursor jedes Mal um 36 Punkte, wenn wir die Tabulatortaste in Microsoft Word drücken.
self.assertEqual(0, len(doc.first_section.body.first_paragraph.get_effective_tab_stops()))
# Wir können benutzerdefinierte Tabstopps in Microsoft Word hinzufügen, wenn wir das Lineal über die Registerkarte "View" aktivieren.
# Jede Einheit auf diesem Lineal entspricht zwei Standard-Tabstopps, also 72 Punkten.
# Wir können benutzerdefinierte Tabstopps programmatisch wie folgt hinzufügen.
tab_stops = doc.first_section.body.first_paragraph.paragraph_format.tab_stops
tab_stops.add(position=72, alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DOTS)
tab_stops.add(position=216, alignment=aw.TabAlignment.CENTER, leader=aw.TabLeader.DASHES)
tab_stops.add(position=360, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.LINE)
# Wir können diese Tabstopps in Microsoft Word sehen, indem wir das Lineal über "View" -> "Show" -> "Ruler" aktivieren.
self.assertEqual(3, len(para.get_effective_tab_stops()))
# Alle Tabulatorzeichen, die wir hinzufügen, nutzen die Tabstopps auf dem Lineal und können,
# abhängig vom Wert des Tab-Leaders, eine Linie zwischen dem Tab-Start- und Zielpunkt hinterlassen.
para.append_child(aw.Run(doc=doc, text='\tTab 1\tTab 2\tTab 3'))
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.TabStops.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

