---
title: ChartDataLabel.left_mode property
linktitle: left_mode property
articleTitle: left_mode property
second_title: Aspose.Words for Python
description: "ChartDataLabel.left_mode property. Gets or sets the interpretation mode of the [ChartDataLabel.left](../left/) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [ChartDataLabel.position](../position/) property."
type: docs
weight: 70
url: /de/python-net/aspose.words.drawing.charts/chartdatalabel/left_mode/
---

## ChartDataLabel.left_mode property

Gets or sets the interpretation mode of the [ChartDataLabel.left](../left/) property value: whether it sets the location
of the data label from the left edge of the chart of from the position specified by its [ChartDataLabel.position](../position/)
property.



```python
@property
def left_mode(self) -> aspose.words.drawing.charts.ChartDataLabelLocationMode:
    ...

@left_mode.setter
def left_mode(self, value: aspose.words.drawing.charts.ChartDataLabelLocationMode):
    ...

```

### Remarks

The property cannot be set in a Word 2016 chart.


### Examples

Shows how to place data labels of doughnut chart outside doughnut.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_width = 432
chart_height = 252
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.DOUGHNUT, width=chart_width, height=chart_height)
chart = shape.chart
series_coll = chart.series
# Standardmäßig generierte Serie löschen.
series_coll.clear()
# Legende ausblenden.
chart.legend.position = aw.drawing.charts.LegendPosition.NONE
# Daten generieren.
data_length = 20
total_value = 0
categories = [None for i in range(0, data_length)]
values = [None for i in range(0, data_length)]
i = 0
while i < data_length:
    categories[i] = f'Category {i}'
    values[i] = data_length - i
    total_value = total_value + values[i]
    i += 1
series = series_coll.add(series_name='Series 1', categories=categories, values=values)
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_value = True
data_labels.show_leader_lines = True
# Die Position-Eigenschaft kann für Donut-Diagramme nicht verwendet werden. Platzieren wir Datenbeschriftungen mit den Left- und Top-
# Eigenschaften um einen Kreis außerhalb des Diagrammdonuts.
# Der Ursprung befindet sich in der oberen linken Ecke des Diagramms.
title_area_height = 25.5  # This can be calculated using title text and font.
doughnut_center_y = title_area_height + (chart_height - title_area_height) / 2
doughnut_center_x = chart_width / 2
label_height = 16.5  # This can be calculated using label font.
one_char_label_width = 12.75  # This can be calculated for each label using its text and font.
two_char_label_width = 17.25  # This can be calculated for each label using its text and font.
y_margin = 0.75
label_margin = 1.5
label_circle_radius = chart_height - doughnut_center_y - y_margin - label_height / 2
# Da die Datenpunkte oben beginnen, werden die X-Koordinaten, die in den Left- und Top-Eigenschaften von
# Die Datenbeschriftungen zeigen nach rechts und die Y‑Koordinaten nach unten, der Startwinkel ist -PI/2.
total_angle = -math.pi / 2
previous_label = None
i = 0
while i < series.y_values.count:
    data_label = data_labels[i]
    value = series.y_values[i].double_value
    label_width = None
    if value < 10:
        label_width = one_char_label_width
    else:
        label_width = two_char_label_width
    label_segment_angle = value / total_value * 2 * math.pi
    label_angle = label_segment_angle / 2 + total_angle
    label_center_x = label_circle_radius * math.cos(label_angle) + doughnut_center_x
    label_center_y = label_circle_radius * math.sin(label_angle) + doughnut_center_y
    label_left = label_center_x - label_width / 2
    label_top = label_center_y - label_height / 2
    # Wenn die aktuelle Datenbeschriftung andere Beschriftungen überlappt, verschieben Sie sie horizontal.
    if previous_label != None and math.fabs(previous_label.top - label_top) < label_height and (math.fabs(previous_label.left - label_left) < label_width):
        # Bewegen Sie nach rechts oben, nach links unten.
        is_on_top = total_angle < 0 or total_angle >= math.pi
        factor = None
        if is_on_top:
            factor = 1
        else:
            factor = -1
        label_left = previous_label.left + label_width * factor + label_margin
    data_label.left = label_left
    data_label.left_mode = aw.drawing.charts.ChartDataLabelLocationMode.ABSOLUTE
    data_label.top = label_top
    data_label.top_mode = aw.drawing.charts.ChartDataLabelLocationMode.ABSOLUTE
    total_angle = total_angle + label_segment_angle
    previous_label = data_label
    i += 1
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DoughnutChartLabelPosition.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabel](../)

