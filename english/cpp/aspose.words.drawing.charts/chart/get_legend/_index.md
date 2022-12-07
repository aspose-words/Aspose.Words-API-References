---
title: get_Legend
second_title: Aspose.Words for C++ API Reference
description: Provides access to the chart legend properties.
type: docs
weight: 53
url: /cpp/aspose.words.drawing.charts/chart/get_legend/
---
## Chart::get_Legend method


Provides access to the chart legend properties.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> Aspose::Words::Drawing::Charts::Chart::get_Legend()
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

* Class [ChartLegend](../../chartlegend/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
