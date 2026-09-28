---
title: ChartLegend.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartLegend.font property. Provides access to the default font formatting of legend entries"
type: docs
weight: 10
url: /zh/python-net/aspose.words.drawing.charts/chartlegend/font/
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
# 设置所有图例项的默认字体大小。
chart_legend.font.size = 14
# 更改特定图例项的字体。
chart_legend.legend_entries[1].font.italic = True
chart_legend.legend_entries[1].font.size = 12
# 获取图表系列的图例项。
legend_entry = chart.series[0].legend_entry
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LegendFont.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartLegend](../)

