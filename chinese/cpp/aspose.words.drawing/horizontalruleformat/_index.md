---
title: "Aspose::Words::Drawing::HorizontalRuleFormat 类"
linktitle: "HorizontalRuleFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::HorizontalRuleFormat 类。表示水平线格式。要了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class


表示水平线格式。要了解更多信息，请访问 [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) 文档文章。

```cpp
class HorizontalRuleFormat : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Alignment](./get_alignment/)() | 获取或设置水平线的对齐方式。 |
| [get_Color](./get_color/)() | 获取或设置填充水平线的画笔颜色。 |
| [get_Height](./get_height/)() | 获取或设置水平线的高度。 |
| [get_NoShade](./get_noshade/)() | 指示水平线是否具有 3D 阴影。如果 **true**，则水平线没有 3D 阴影，使用纯色。 |
| [get_WidthPercent](./get_widthpercent/)() | 获取或设置指定水平线的长度，以窗口宽度的百分比表示。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::Drawing::HorizontalRuleAlignment) | 用于设置 [Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment](./get_alignment/) 的 setter。 |
| [set_Color](./set_color/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Drawing::HorizontalRuleFormat::get_Color](./get_color/) 的 setter。 |
| [set_Height](./set_height/)(double) | 用于设置 [Aspose::Words::Drawing::HorizontalRuleFormat::get_Height](./get_height/) 的 setter。 |
| [set_NoShade](./set_noshade/)(bool) | 用于设置 [Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade](./get_noshade/) 的 setter。 |
| [set_WidthPercent](./set_widthpercent/)(double) | 用于设置 [Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent](./get_widthpercent/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示如何插入水平线形状并自定义其格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertHorizontalRule();

System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> horizontalRuleFormat = shape->get_HorizontalRuleFormat();
horizontalRuleFormat->set_Alignment(Aspose::Words::Drawing::HorizontalRuleAlignment::Center);
horizontalRuleFormat->set_WidthPercent(70);
horizontalRuleFormat->set_Height(3);
horizontalRuleFormat->set_Color(System::Drawing::Color::get_Blue());
horizontalRuleFormat->set_NoShade(true);

ASSERT_TRUE(shape->get_IsHorizontalRule());
ASSERT_TRUE(shape->get_HorizontalRuleFormat()->get_NoShade());
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
