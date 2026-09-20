---
title: "Aspose::Words::Drawing::Charts::ChartTitle 类"
linktitle: "ChartTitle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartTitle 类。提供对图表标题属性的访问。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class


提供对图表标题属性的访问。要了解更多，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

```cpp
class ChartTitle : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Font](./get_font/)() | 提供对图表标题字体格式的访问。 |
| [get_Format](./get_format/)() | 提供对图表标题填充和线条格式的访问。 |
| [get_Orientation](./get_orientation/)() | 获取或设置图表标题文本的方向。 |
| [get_Overlay](./get_overlay/)() | 确定是否允许其他图表元素覆盖标题。默认情况下，覆盖为 **false**。 |
| [get_Rotation](./get_rotation/)() | 获取或设置图表标题的旋转角度（以度为单位）。 |
| [get_Show](./get_show/)() | 确定是否在此图表中显示标题。默认值为 **true**。 |
| [get_Text](./get_text/)() | 获取或设置图表标题的文本。如果指定 **null** 或空值，将显示自动生成的标题。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | 用于 [Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation](./get_orientation/) 的 setter。 |
| [set_Overlay](./set_overlay/)(bool) | 用于 [Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay](./get_overlay/) 的 setter。 |
| [set_Rotation](./set_rotation/)(int32_t) | 用于 [Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation](./get_rotation/) 的 setter。 |
| [set_Show](./set_show/)(bool) | 用于 [Aspose::Words::Drawing::Charts::ChartTitle::get_Show](./get_show/) 的 setter。 |
| [set_Text](./set_text/)(const System::String\&) | 用于 [Aspose::Words::Drawing::Charts::ChartTitle::get_Text](./get_text/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示如何插入图表并设置标题。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用文档生成器插入图表形状并获取其图表。
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// 使用 "Title" 属性为我们的图表添加标题，标题显示在图表区域的顶部中心。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// 将 "Show" 属性设置为 "true"，使标题可见。
title->set_Show(true);

// 将 "Overlay" 属性设置为 "true"，通过允许标题被覆盖，为其他图表元素提供更多空间。
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
