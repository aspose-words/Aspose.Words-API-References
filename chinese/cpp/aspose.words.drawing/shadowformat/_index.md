---
title: "Aspose::Words::Drawing::ShadowFormat class"
linktitle: "ShadowFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShadowFormat 类。表示对象的阴影格式。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.drawing/shadowformat/
---
## ShadowFormat class


表示对象的阴影格式。要了解更多信息，请访问 [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/) 文档文章。

```cpp
class ShadowFormat : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clear](./clear/)() | 清除阴影格式。 |
| [get_Color](./get_color/)() | 获取或设置一个 **Color** 对象，表示阴影的颜色。默认值是 **Black**。 |
| [get_Transparency](./get_transparency/)() | 获取或设置阴影效果的透明度程度，取值范围为 0.0（不透明）到 1.0（透明）。默认值为 0.0。 |
| [get_Type](./get_type/)() | 获取或设置指定的 [ShadowType](../shadowtype/) 用于 [ShadowFormat](./)。 |
| [get_Visible](./get_visible/)() | 如果应用于此实例的格式可见，则返回 **true**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | 用于 [Aspose::Words::Drawing::ShadowFormat::get_Color](./get_color/) 的设置器。 |
| [set_Transparency](./set_transparency/)(double) | 用于 [Aspose::Words::Drawing::ShadowFormat::get_Transparency](./get_transparency/) 的设置器。 |
| [set_Type](./set_type/)(Aspose::Words::Drawing::ShadowType) | 用于 [Aspose::Words::Drawing::ShadowFormat::get_Type](./get_type/) 的设置器。 |
| static [Type](./type/)() |  |

## 示例



展示如何获取阴影颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
