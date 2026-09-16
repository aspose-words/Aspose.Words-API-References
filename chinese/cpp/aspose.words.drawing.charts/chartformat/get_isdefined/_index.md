---
title: "Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined 方法"
linktitle: "get_IsDefined"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined 方法。获取一个标志，指示在 C++ 中是否定义了任何格式。"
type: docs
weight: 2250
url: /zh/cpp/aspose.words.drawing.charts/chartformat/get_isdefined/
---
## ChartFormat::get_IsDefined method


获取指示是否已定义任何格式的标志。

```cpp
bool Aspose::Words::Drawing::Charts::ChartFormat::get_IsDefined()
```


## 示例



展示如何将填充重置为系列中定义的默认值。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = series->get_DataPoints()->idx_get(1);

ASSERT_TRUE(dataPoint->get_Format()->get_IsDefined());

dataPoint->get_Format()->SetDefaultFill();

doc->Save(get_ArtifactsDir() + u"Charts.ResetDataPointFill.docx");
```

## 另见

* Class [ChartFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
