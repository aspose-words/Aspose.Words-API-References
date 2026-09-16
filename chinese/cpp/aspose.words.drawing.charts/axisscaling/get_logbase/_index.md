---
title: "Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase 方法"
linktitle: "get_LogBase"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase 方法。获取或设置对数坐标轴的对数基数，在 C++ 中。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.drawing.charts/axisscaling/get_logbase/
---
## AxisScaling::get_LogBase method


获取或设置对数轴的对数基数。

```cpp
double Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase() const
```

## 备注


此属性不受 MS Office 2016 新图表的支持。

浮点值的有效范围大于等于 2 且小于等于 1000。仅当 [Type](../get_type/) 设置为 [Logarithmic](../../axisscaletype/) 时，此属性才生效。

设置此属性会将 [Type](../get_type/) 属性设置为 [Logarithmic](../../axisscaletype/)。

## 示例



展示如何将对数缩放应用于图表坐标轴。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// 清除图表的演示数据系列，以便从空白图表开始。
chart->get_Series()->Clear();

// 插入一个包含五个点的 X/Y 坐标系列。
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), System::MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// X 轴的比例默认是线性的，
// 显示均匀递增的数值，覆盖我们的 X 值范围 (0, 1, 2, 3...)。
// 线性坐标轴并不适合我们的 Y 值
// 因为较小的 Y 值点将更难阅读。
// 基数为 20 的对数缩放 (1, 20, 400, 8000...)
// 将展开绘制的点，使我们能够更容易地读取图表上的数值。
chart->get_AxisY()->get_Scaling()->set_Type(Aspose::Words::Drawing::Charts::AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(get_ArtifactsDir() + u"Charts.AxisScaling.docx");
```

## 另见

* Class [AxisScaling](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
