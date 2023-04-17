---
title: Aspose::Words::Drawing::Charts::LegendPosition enum
linktitle: LegendPosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::LegendPosition enum. Specifies the possible positions for a chart legend in C++.'
type: docs
weight: 29000
url: /cpp/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enum


Specifies the possible positions for a chart legend.

```cpp
enum class LegendPosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | No legend will be shown for the chart. |
| Bottom | 1 | Specifies that the legend shall be drawn at the bottom of the chart. |
| Left | 2 | Specifies that the legend shall be drawn at the left of the chart. |
| Right | 3 | Specifies that the legend shall be drawn at the right of the chart. |
| Top | 4 | Specifies that the legend shall be drawn at the top of the chart. |
| TopRight | 5 | Specifies that the legend shall be drawn at the top right of the chart. |


## Examples



Shows how to edit the appearance of a chart's legend. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Line, 450, 300);
SharedPtr<Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Move the chart's legend to the top right corner.
SharedPtr<ChartLegend> legend = chart->get_Legend();
legend->set_Position(LegendPosition::TopRight);

// Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
legend->set_Overlay(true);

doc->Save(ArtifactsDir + u"Charts.ChartLegend.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
