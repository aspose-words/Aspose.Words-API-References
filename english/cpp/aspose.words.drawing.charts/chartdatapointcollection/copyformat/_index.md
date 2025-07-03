---
title: Aspose::Words::Drawing::Charts::ChartDataPointCollection::CopyFormat method
linktitle: CopyFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataPointCollection::CopyFormat method. Copies format from the source data point to the destination data point in C++.'
type: docs
weight: 2500
url: /cpp/aspose.words.drawing.charts/chartdatapointcollection/copyformat/
---
## ChartDataPointCollection::CopyFormat method


Copies format from the source data point to the destination data point.

```cpp
void Aspose::Words::Drawing::Charts::ChartDataPointCollection::CopyFormat(int32_t sourceIndex, int32_t destinationIndex)
```


## Examples



Shows how to copy data point format. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

// Get the chart and series to update format.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_FALSE(dataPoints->HasDefaultFormat(1));

// Copy format of the data point with index 1 to the data point with index 2
// so that the data point 2 looks the same as the data point 1.
dataPoints->CopyFormat(0, 1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

// Copy format of the data point with index 0 to the series defaults so that all data points
// in the series that have the default format look the same as the data point 0.
series->CopyFormatFrom(1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

doc->Save(get_ArtifactsDir() + u"Charts.CopyDataPointFormat.docx");
```

## See Also

* Class [ChartDataPointCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
