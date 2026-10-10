---
title: "Aspose::Words::Drawing::Charts::ChartDataPointCollection::CopyFormat 方法"
linktitle: "CopyFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataPointCollection::CopyFormat 方法。在 C++ 中将从源数据点复制格式到目标数据点。"
type: docs
weight: 2500
url: /zh/cpp/aspose.words.drawing.charts/chartdatapointcollection/copyformat/
---
## ChartDataPointCollection::CopyFormat method


将格式从源数据点复制到目标数据点。

```cpp
void Aspose::Words::Drawing::Charts::ChartDataPointCollection::CopyFormat(int32_t sourceIndex, int32_t destinationIndex)
```


## 示例



展示如何复制数据点格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

// 获取图表和系列以更新格式。
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_FALSE(dataPoints->HasDefaultFormat(1));

// 将索引为 1 的数据点的格式复制到索引为 2 的数据点
// 使数据点 2 看起来与数据点 1 相同。
dataPoints->CopyFormat(0, 1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

// 将索引为 0 的数据点的格式复制到系列默认设置，以便所有数据点
// 在系列中具有默认格式的所有数据点看起来与数据点 0 相同。
series->CopyFormatFrom(1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

doc->Save(get_ArtifactsDir() + u"Charts.CopyDataPointFormat.docx");
```

## 另见

* Class [ChartDataPointCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
