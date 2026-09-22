---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Color طريقة"
linktitle: "get_Color"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Color طريقة. تسترجع أو تعيّن لون الفرشاة الذي يملأ الخط الأفقي في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.drawing/horizontalruleformat/get_color/
---
## HorizontalRuleFormat::get_Color method


يحصل أو يضبط لون الفرشاة الذي يملأ الخط الأفقي.

```cpp
System::Drawing::Color Aspose::Words::Drawing::HorizontalRuleFormat::get_Color()
```

## ملاحظات


هذا اختصار إلى الخاصية [Color](../../fill/get_color/).

القيمة الافتراضية هي **Gray**.

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
