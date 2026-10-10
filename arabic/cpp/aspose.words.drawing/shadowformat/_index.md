---
title: "Aspose::Words::Drawing::ShadowFormat class"
linktitle: "ShadowFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShadowFormat class. يمثل تنسيق الظل لكائن. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.drawing/shadowformat/
---
## ShadowFormat class


يمثل تنسيق الظل لكائن. لمعرفة المزيد، زر مقالة الوثائق [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class ShadowFormat : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clear](./clear/)() | يمسح تنسيق الظل. |
| [get_Color](./get_color/)() | يحصل أو يعيّن كائن **Color** الذي يمثل لون الظل. القيمة الافتراضية هي **Black**. |
| [get_Transparency](./get_transparency/)() | يحصل أو يعيّن درجة الشفافية لتأثير الظل كقيمة بين 0.0 (معتم) و 1.0 (شفاف). القيمة الافتراضية هي 0.0. |
| [get_Type](./get_type/)() | يحصل أو يعيّن [ShadowType](../shadowtype/) المحدد لـ [ShadowFormat](./). |
| [get_Visible](./get_visible/)() | يرجع **true** إذا كان التنسيق المطبق على هذه الحالة مرئيًا. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Drawing::ShadowFormat::get_Color](./get_color/). |
| [set_Transparency](./set_transparency/)(double) | مُعيّن لـ [Aspose::Words::Drawing::ShadowFormat::get_Transparency](./get_transparency/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::ShadowType) | مُعيّن لـ [Aspose::Words::Drawing::ShadowFormat::get_Type](./get_type/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية الحصول على لون الظل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
