---
title: "Aspose::Words::Drawing::Charts::AxisScaling 类"
linktitle: "AxisScaling"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::AxisScaling 类。表示轴的缩放选项。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class


表示轴的缩放选项。欲了解更多信息，请访问 [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) 文档文章。

```cpp
class AxisScaling : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [AxisScaling](./axisscaling/)() |  |
| [get_LogBase](./get_logbase/)() const | 获取或设置对数轴的对数基数。 |
| [get_Maximum](./get_maximum/)() | 获取或设置轴的最大值。 |
| [get_Minimum](./get_minimum/)() | 获取或设置轴的最小值。 |
| [get_Type](./get_type/)() const | 获取或设置轴的缩放类型。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_LogBase](./set_logbase/)(double) | 用于 [Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase](./get_logbase/) 的 setter。 |
| [set_Maximum](./set_maximum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | 用于设置 [Aspose::Words::Drawing::Charts::AxisScaling::get_Maximum](./get_maximum/)。 |
| [set_Minimum](./set_minimum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | 用于设置 [Aspose::Words::Drawing::Charts::AxisScaling::get_Minimum](./get_minimum/)。 |
| [set_Type](./set_type/)(Aspose::Words::Drawing::Charts::AxisScaleType) | 用于设置 [Aspose::Words::Drawing::Charts::AxisScaling::get_Type](./get_type/)。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
