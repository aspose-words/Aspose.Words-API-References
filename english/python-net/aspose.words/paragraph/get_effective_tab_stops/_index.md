---
title: Paragraph.get_effective_tab_stops method
linktitle: get_effective_tab_stops method
articleTitle: get_effective_tab_stops method
second_title: Aspose.Words for Python
description: "Paragraph.get_effective_tab_stops method. Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists."
type: docs
weight: 270
url: /python-net/aspose.words/paragraph/get_effective_tab_stops/
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

# If we are in a paragraph with no tab stops in this collection,
# the cursor will jump 36 points each time we press the Tab key in Microsoft Word.
self.assertEqual(0, doc.first_section.body.first_paragraph.get_effective_tab_stops().length)

# We can add custom tab stops in Microsoft Word if we enable the ruler via the "View" tab.
# Each unit on this ruler is two default tab stops, which is 72 points.
# We can add custom tab stops programmatically like this.
tab_stops = doc.first_section.body.first_paragraph.paragraph_format.tab_stops
tab_stops.add(72, aw.TabAlignment.LEFT, aw.TabLeader.DOTS)
tab_stops.add(216, aw.TabAlignment.CENTER, aw.TabLeader.DASHES)
tab_stops.add(360, aw.TabAlignment.RIGHT, aw.TabLeader.LINE)

# We can see these tab stops in Microsoft Word by enabling the ruler via "View" -> "Show" -> "Ruler".
self.assertEqual(3, para.get_effective_tab_stops().length)

# Any tab characters we add will make use of the tab stops on the ruler and may,
# depending on the tab leader's value, leave a line between the tab departure and arrival destinations.
para.append_child(aw.Run(doc, "\tTab 1\tTab 2\tTab 3"))

doc.save(ARTIFACTS_DIR + "Paragraph.tab_stops.docx")
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

