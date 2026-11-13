---
title: ChartLegend.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartLegend.font property. Provides access to the default font formatting of legend entries"
type: docs
weight: 10
url: /es/python-net/aspose.words.drawing.charts/chartlegend/font/
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
# Establecer el tamaño de fuente predeterminado para todas las entradas de la leyenda.
chart_legend.font.size = 14
# Cambiar la fuente para una entrada de leyenda específica.
chart_legend.legend_entries[1].font.italic = True
chart_legend.legend_entries[1].font.size = 12
# Obtener la entrada de la leyenda para la serie del gráfico.
legend_entry = chart.series[0].legend_entry
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LegendFont.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartLegend](../)

