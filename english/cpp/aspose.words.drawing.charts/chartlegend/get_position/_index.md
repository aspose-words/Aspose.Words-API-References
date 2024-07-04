---
title: Aspose::Words::Drawing::Charts::ChartLegend::get_Position method
linktitle: get_Position
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartLegend::get_Position method. Specifies the position of the legend on a chart. Default value is Right in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.drawing.charts/chartlegend/get_position/
---
## ChartLegend::get_Position method


Specifies the position of the legend on a chart. Default value is [Right](../../legendposition/).

```cpp
Aspose::Words::Drawing::Charts::LegendPosition Aspose::Words::Drawing::Charts::ChartLegend::get_Position()
```


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

* Enum [LegendPosition](../../legendposition/)
* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
