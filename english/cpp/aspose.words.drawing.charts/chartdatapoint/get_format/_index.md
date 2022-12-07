---
title: get_Format
second_title: Aspose.Words for C++ API Reference
description: Provides access to fill and line formatting of this data point.
type: docs
weight: 53
url: /cpp/aspose.words.drawing.charts/chartdatapoint/get_format/
---
## ChartDataPoint::get_Format method


Provides access to fill and line formatting of this data point.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartDataPoint::get_Format()
```


## Examples



Shows how to set individual formatting for categories of a column chart. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Column, 432, 252);
SharedPtr<Chart> chart = shape->get_Chart();

// Delete default generated series.
chart->get_Series()->Clear();

// Adding new series.
SharedPtr<ChartSeries> series = chart->get_Series()->Add(u"Series 1", MakeArray<String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"}),
                                                         MakeArray<double>({1, 2, 3, 4}));

// Set column formatting.
SharedPtr<ChartDataPointCollection> dataPoints = series->get_DataPoints();
dataPoints->idx_get(0)->get_Format()->get_Fill()->PresetTextured(PresetTexture::Denim);
dataPoints->idx_get(1)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
dataPoints->idx_get(2)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Blue());

doc->Save(ArtifactsDir + u"Charts.DataPointsFormatting.docx");
```

## See Also

* Class [ChartFormat](../../chartformat/)
* Class [ChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
