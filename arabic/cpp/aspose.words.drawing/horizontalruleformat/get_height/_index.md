---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height طريقة"
linktitle: "get_Height"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height طريقة. تسترجع أو تعيّن ارتفاع الخط الأفقي في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing/horizontalruleformat/get_height/
---
## HorizontalRuleFormat::get_Height method


يحصل أو يضبط ارتفاع الخط الأفقي.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_Height()
```

## ملاحظات


هذا اختصار إلى الخاصية [Height](../../shapebase/get_height/).

القيم الصالحة تتراوح من 0 إلى 1584 شاملًا.

القيمة الافتراضية هي 1.5.

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
