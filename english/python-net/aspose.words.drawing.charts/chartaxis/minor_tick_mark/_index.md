---
title: ChartAxis.minor_tick_mark property
linktitle: minor_tick_mark property
articleTitle: minor_tick_mark property
second_title: Aspose.Words for Python
description: "ChartAxis.minor_tick_mark property. Returns or sets the minor tick marks for the axis."
type: docs
weight: 160
url: /python-net/aspose.words.drawing.charts/chartaxis/minor_tick_mark/
---

## ChartAxis.minor_tick_mark property

Returns or sets the minor tick marks for the axis.


```python
@property
def minor_tick_mark(self) -> aspose.words.drawing.charts.AxisTickMark:
    ...

@minor_tick_mark.setter
def minor_tick_mark(self, value: aspose.words.drawing.charts.AxisTickMark):
    ...

```

### Examples

Shows how to insert a chart and modify the appearance of its axes.

```python
import aspose.words as aw
from aspose.pydrawing import Color
from api_example_base import ApiExampleBase, ARTIFACTS_DIR

class TestChartAxisProperties(ApiExampleBase):

    def test_chart_axis_properties(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=500, height=300)
        chart = shape.chart
        # Clear the chart's demo data series to start with a clean chart.
        chart.series.clear()
        # Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
        chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel', 'GoogleDocs', 'Note'], values=[640, 320, 280, 120, 150])
        # Chart axes have various options that can change their appearance,
        # such as their direction, major/minor unit ticks, and tick marks.
        x_axis = chart.axis_x
        x_axis.category_type = aw.drawing.charts.AxisCategoryType.CATEGORY
        x_axis.crosses = aw.drawing.charts.AxisCrosses.MINIMUM
        x_axis.reverse_order = False
        x_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.INSIDE
        x_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
        x_axis.major_unit = 10
        x_axis.minor_unit = 15
        x_axis.tick_labels.offset = 50
        x_axis.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.LOW
        x_axis.tick_labels.is_auto_spacing = False
        x_axis.tick_mark_spacing = 1
        self.assertEqual(doc, x_axis.document)
        y_axis = chart.axis_y
        y_axis.category_type = aw.drawing.charts.AxisCategoryType.AUTOMATIC
        y_axis.crosses = aw.drawing.charts.AxisCrosses.MAXIMUM
        y_axis.reverse_order = True
        y_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.INSIDE
        y_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
        y_axis.major_unit = 100
        y_axis.minor_unit = 20
        y_axis.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.NEXT_TO_AXIS
        y_axis.tick_labels.alignment = aw.ParagraphAlignment.CENTER
        y_axis.tick_labels.font.color = Color.red
        y_axis.tick_labels.spacing = 1
        # Column charts do not have a Z-axis.
        self.assertIsNone(chart.axis_z)
        doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisProperties.docx')
        doc = aw.Document(file_name=ARTIFACTS_DIR + 'Charts.AxisProperties.docx')
        chart = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().chart
        self.assertEqual(aw.drawing.charts.AxisCategoryType.CATEGORY, chart.axis_x.category_type)
        self.assertEqual(aw.drawing.charts.AxisCrosses.MINIMUM, chart.axis_x.crosses)
        self.assertFalse(chart.axis_x.reverse_order)
        self.assertEqual(aw.drawing.charts.AxisTickMark.INSIDE, chart.axis_x.major_tick_mark)
        self.assertEqual(aw.drawing.charts.AxisTickMark.CROSS, chart.axis_x.minor_tick_mark)
        self.assertEqual(1, chart.axis_x.major_unit)
        self.assertEqual(0.5, chart.axis_x.minor_unit)
        self.assertEqual(50, chart.axis_x.tick_labels.offset)
        self.assertEqual(aw.drawing.charts.AxisTickLabelPosition.LOW, chart.axis_x.tick_labels.position)
        self.assertFalse(chart.axis_x.tick_labels.is_auto_spacing)
        self.assertEqual(1, chart.axis_x.tick_mark_spacing)
        self.assertTrue(chart.axis_x.format.is_defined)
        self.assertEqual(aw.drawing.charts.AxisCategoryType.CATEGORY, chart.axis_y.category_type)
        self.assertEqual(aw.drawing.charts.AxisCrosses.MAXIMUM, chart.axis_y.crosses)
        self.assertTrue(chart.axis_y.reverse_order)
        self.assertEqual(aw.drawing.charts.AxisTickMark.INSIDE, chart.axis_y.major_tick_mark)
        self.assertEqual(aw.drawing.charts.AxisTickMark.CROSS, chart.axis_y.minor_tick_mark)
        self.assertEqual(100, chart.axis_y.major_unit)
        self.assertEqual(20, chart.axis_y.minor_unit)
        self.assertEqual(aw.drawing.charts.AxisTickLabelPosition.NEXT_TO_AXIS, chart.axis_y.tick_labels.position)
        self.assertEqual(aw.ParagraphAlignment.CENTER, chart.axis_y.tick_labels.alignment)
        self.assertEqual(Color.red.to_argb(), chart.axis_y.tick_labels.font.color.to_argb())
        self.assertEqual(1, chart.axis_y.tick_labels.spacing)
        self.assertTrue(chart.axis_y.format.is_defined)
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

