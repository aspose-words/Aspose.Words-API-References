---
title: "Aspose::Words::Drawing::HorizontalRuleFormat فئة"
linktitle: "HorizontalRuleFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat فئة. يمثل تنسيق الخط الأفقي. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class


يمثل تنسيق القاعدة الأفقية. لمعرفة المزيد، زر مقالة الوثائق [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class HorizontalRuleFormat : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Alignment](./get_alignment/)() | يحصل أو يضبط محاذاة الخط الأفقي. |
| [get_Color](./get_color/)() | يحصل أو يضبط لون الفرشاة الذي يملأ الخط الأفقي. |
| [get_Height](./get_height/)() | يحصل أو يضبط ارتفاع الخط الأفقي. |
| [get_NoShade](./get_noshade/)() | يشير إلى وجود تظليل ثلاثي الأبعاد للخط الأفقي. إذا كان **true**، فإن الخط الأفقي يكون بدون تظليل ثلاثي الأبعاد ويُستخدم لون صلب. |
| [get_WidthPercent](./get_widthpercent/)() | يحصل أو يضبط طول الخط الأفقي المحدد معبرًا عنه كنسبة مئوية من عرض النافذة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::Drawing::HorizontalRuleAlignment) | المُعدِّل لـ [Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment](./get_alignment/). |
| [set_Color](./set_color/)(System::Drawing::Color) | محدد لـ [Aspose::Words::Drawing::HorizontalRuleFormat::get_Color](./get_color/). |
| [set_Height](./set_height/)(double) | محدد لـ [Aspose::Words::Drawing::HorizontalRuleFormat::get_Height](./get_height/). |
| [set_NoShade](./set_noshade/)(bool) | محدد لـ [Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade](./get_noshade/). |
| [set_WidthPercent](./set_widthpercent/)(double) | محدد لـ [Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent](./get_widthpercent/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية إدراج شكل قاعدة أفقية وتخصيص تنسيقه.
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

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
