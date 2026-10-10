---
title: "Aspose::Words::Drawing::HorizontalRuleAlignment enum"
linktitle: "HorizontalRuleAlignment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::HorizontalRuleAlignment enum. يمثل محاذاة القاعدة الأفقية المحددة في C++."
type: docs
weight: 27000
url: /ar/cpp/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enum


يمثل المحاذاة للقاعدة الأفقية المحددة.

```cpp
enum class HorizontalRuleAlignment
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| يسار | 0 | محاذاة إلى اليسار. |
| وسط | 1 | محاذاة إلى الوسط. |
| يمين | 2 | محاذاة إلى اليمين. |


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
