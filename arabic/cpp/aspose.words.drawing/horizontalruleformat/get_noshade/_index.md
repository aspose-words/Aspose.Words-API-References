---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade طريقة"
linktitle: "get_NoShade"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade method. يشير إلى وجود تظليل ثلاثي الأبعاد للخط الأفقي. إذا كان true، فإن الخط الأفقي يكون بدون تظليل ثلاثي الأبعاد ويُستخدم لون صلب في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.drawing/horizontalruleformat/get_noshade/
---
## HorizontalRuleFormat::get_NoShade method


يشير إلى وجود تظليل ثلاثي الأبعاد للخط الأفقي. إذا كان **true**، فإن الخط الأفقي يكون بدون تظليل ثلاثي الأبعاد ويُستخدم لون صلب.

```cpp
bool Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade()
```

## ملاحظات


القيمة الافتراضية هي **false**.

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
