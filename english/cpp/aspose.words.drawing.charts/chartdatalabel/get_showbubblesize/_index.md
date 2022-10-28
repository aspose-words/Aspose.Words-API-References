---
title: get_ShowBubbleSize
second_title: Aspose.Words for C++ API Reference
description: Allows to specify if bubble size is to be displayed for the data labels on a chart. Applies only to Bubble charts. Default value is false.
type: docs
weight: 79
url: /cpp/aspose.words.drawing.charts/chartdatalabel/get_showbubblesize/
---
## ChartDataLabel.get_ShowBubbleSize method


Allows to specify if bubble size is to be displayed for the data labels on a chart. Applies only to Bubble charts. Default value is false.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize()
```


## Examples




Shows how to use 3D effects with bubble charts. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Bubble3D, 500, 350);
SharedPtr<Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_TRUE(chart->get_Series()->idx_get(0)->get_Bubble3D());

// Apply a data label to each bubble that displays its diameter.
for (int i = 0; i < 3; i++)
{
    chart->get_Series()->idx_get(0)->set_HasDataLabels(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->set_ShowBubbleSize(true);
}

doc->Save(ArtifactsDir + u"Charts.Bubble3D.docx");
```

