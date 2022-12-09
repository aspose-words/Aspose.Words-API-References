---
title: get_Explosion
second_title: Aspose.Words for C++ API Reference
description: Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts.
type: docs
weight: 40
url: /cpp/aspose.words.drawing.charts/chartdatapoint/get_explosion/
---
## ChartDataPoint::get_Explosion method


Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion() override
```


## Examples



Shows how to move the slices of a pie chart away from the center. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Pie, 500, 350);
SharedPtr<Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Sales", chart->get_Series()->idx_get(0)->get_Name());

// "Slices" of a pie chart may be moved away from the center by a distance via the respective data point's Explosion attribute.
// Add a data point to the first portion of the pie chart and move it away from the center by 10 points.
// Aspose.Words create data points automatically if them does not exist.
SharedPtr<ChartDataPoint> dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(0);
dataPoint->set_Explosion(10);

// Displace the second portion by a greater distance.
dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(1);
dataPoint->set_Explosion(40);

doc->Save(ArtifactsDir + u"Charts.PieChartExplosion.docx");
```

## See Also

* Class [ChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
