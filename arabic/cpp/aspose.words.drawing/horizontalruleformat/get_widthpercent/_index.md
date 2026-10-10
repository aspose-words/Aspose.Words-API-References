---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent طريقة"
linktitle: "get_WidthPercent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent طريقة. يحصل أو يحدد طول الخط الأفقي المحدد معبرًا عنه كنسبة مئوية من عرض النافذة في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.drawing/horizontalruleformat/get_widthpercent/
---
## HorizontalRuleFormat::get_WidthPercent method


يحصل أو يضبط طول الخط الأفقي المحدد معبرًا عنه كنسبة مئوية من عرض النافذة.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent()
```

## ملاحظات


القيم الصالحة تتراوح من 1 إلى 100 شاملًا.

القيمة الافتراضية هي 100.

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

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
