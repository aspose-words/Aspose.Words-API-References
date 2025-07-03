---
title: Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay method
linktitle: get_Overlay
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay method. Determines whether other chart elements shall be allowed to overlap legend. Default value is false in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.drawing.charts/chartlegend/get_overlay/
---
## ChartLegend::get_Overlay method


Determines whether other chart elements shall be allowed to overlap legend. Default value is **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay() const
```


## Examples



Shows how to edit the appearance of a chart's legend. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Move the chart's legend to the top right corner.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## See Also

* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
