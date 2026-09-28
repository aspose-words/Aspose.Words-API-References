---
title: ChartLegendEntry.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartLegendEntry.font property. Provides access to the font formatting of this legend entry."
type: docs
weight: 10
url: /de/python-net/aspose.words.drawing.charts/chartlegendentry/font/
---

## ChartLegendEntry.font property

Provides access to the font formatting of this legend entry.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Examples

Shows how to work with a legend font.

```python
doc = aw.Document(file_name=MY_DIR + 'Reporting engine template - Chart series.docx')
chart = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().chart
chart_legend = chart.legend
# Standard-Schriftgröße für alle Legendeeinträge festlegen.
chart_legend.font.size = 14
# Schriftart für einen bestimmten Legendeeintrag ändern.
chart_legend.legend_entries[1].font.italic = True
chart_legend.legend_entries[1].font.size = 12
# Legendeeintrag für Diagrammserie abrufen.
legend_entry = chart.series[0].legend_entry
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LegendFont.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartLegendEntry](../)

