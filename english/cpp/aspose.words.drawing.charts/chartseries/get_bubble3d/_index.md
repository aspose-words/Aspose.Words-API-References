---
title: Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D method
linktitle: get_Bubble3D
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D method. Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.drawing.charts/chartseries/get_bubble3d/
---
## ChartSeries::get_Bubble3D method


Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.

```cpp
bool Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D() override
```


## Examples



Shows how to use 3D effects with bubble charts. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_TRUE(chart->get_Series()->idx_get(0)->get_Bubble3D());

// Apply a data label to each bubble that displays its diameter.
for (int32_t i = 0; i < 3; i++)
{
    chart->get_Series()->idx_get(0)->set_HasDataLabels(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->set_ShowBubbleSize(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->get_Font()->set_Size(12);
}

doc->Save(get_ArtifactsDir() + u"Charts.Bubble3D.docx");
```

## See Also

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
