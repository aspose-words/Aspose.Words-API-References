---
title: "Aspose::Words::Drawing::Charts::ChartXValue::FromString 方法"
linktitle: "FromString"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartXValue::FromString 方法。创建一个类型为 String 的 ChartXValue 实例（C++）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue::FromString method


创建一个 [ChartXValue](../) 实例，类型为 [String](../../chartxvaluetype/)。

```cpp
static System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> Aspose::Words::Drawing::Charts::ChartXValue::FromString(const System::String &value)
```


## 示例



展示如何添加/删除图表数据值。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department1Series = chart->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department2Series = chart->get_Series()->idx_get(1);

// 删除两个系列中的第一个值。
department1Series->Remove(0);
department2Series->Remove(0);

// 向两个系列添加新值。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> newXCategory = Aspose::Words::Drawing::Charts::ChartXValue::FromString(u"Q1, 2023");
department1Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10.3));
department2Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5.7));

doc->Save(get_ArtifactsDir() + u"Charts.ChartDataValues.docx");
```

## 另见

* Class [ChartXValue](../)
* Class [ChartXValue](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
