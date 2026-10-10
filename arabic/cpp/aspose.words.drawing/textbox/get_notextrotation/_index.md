---
title: "طريقة Aspose::Words::Drawing::TextBox::get_NoTextRotation"
linktitle: "get_NoTextRotation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::TextBox::get_NoTextRotation. تحصل أو تعين قيمة منطقية تشير إلى ما إذا كان نص الـ TextBox يجب ألا يدور عندما يدور الشكل في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.drawing/textbox/get_notextrotation/
---
## TextBox::get_NoTextRotation method


تحصل أو تعين قيمة منطقية تشير إلى ما إذا كان نص الـ [TextBox](../) يجب ألا يدور عندما يدور الشكل.

```cpp
bool Aspose::Words::Drawing::TextBox::get_NoTextRotation()
```

## ملاحظات


القيمة الافتراضية هي **false**

## أمثلة



يوضح كيفية تعطيل دوران النص عندما يتم تدوير الشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 20, 20);
shape->get_TextBox()->set_NoTextRotation(true);

doc->Save(get_ArtifactsDir() + u"Shape.NoTextRotation.docx");
```

## انظر أيضًا

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
