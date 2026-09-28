---
title: ChartLegend.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartLegend.font property. Provides access to the default font formatting of legend entries"
type: docs
weight: 10
url: /ar/python-net/aspose.words.drawing.charts/chartlegend/font/
---

## ChartLegend.font property

Provides access to the default font formatting of legend entries. To override the font formatting for
a specific legend entry, use the[ChartLegendEntry.font](../../chartlegendentry/font/) property.



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
# حدد حجم الخط الافتراضي لجميع عناصر الأسطورة.
chart_legend.font.size = 14
# غيّر الخط لعنصر أسطورة محدد.
chart_legend.legend_entries[1].font.italic = True
chart_legend.legend_entries[1].font.size = 12
# احصل على عنصر الأسطورة لسلسلة المخطط.
legend_entry = chart.series[0].legend_entry
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LegendFont.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartLegend](../)

