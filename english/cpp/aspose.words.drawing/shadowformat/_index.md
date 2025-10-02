---
title: Aspose::Words::Drawing::ShadowFormat class
linktitle: ShadowFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShadowFormat class. Represents shadow formatting for an object. To learn more, visit the  documentation article in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.drawing/shadowformat/
---
## ShadowFormat class


Represents shadow formatting for an object. To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/) documentation article.

```cpp
class ShadowFormat : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Clear](./clear/)() | Clears shadow format. |
| [get_Color](./get_color/)() | Gets or sets a **Color** object that represents the color for the shadow. The default value is **Black**. |
| [get_Transparency](./get_transparency/)() | Gets or sets the degree of transparency for the shadow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0. |
| [get_Type](./get_type/)() | Gets or sets the specified [ShadowType](../shadowtype/) for [ShadowFormat](./). |
| [get_Visible](./get_visible/)() | Returns **true** if the formatting applied to this instance is visible. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter for [Aspose::Words::Drawing::ShadowFormat::get_Color](./get_color/). |
| [set_Transparency](./set_transparency/)(double) | Setter for [Aspose::Words::Drawing::ShadowFormat::get_Transparency](./get_transparency/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::ShadowType) | Setter for [Aspose::Words::Drawing::ShadowFormat::get_Type](./get_type/). |
| static [Type](./type/)() |  |

## Examples



Shows how to get shadow color. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
