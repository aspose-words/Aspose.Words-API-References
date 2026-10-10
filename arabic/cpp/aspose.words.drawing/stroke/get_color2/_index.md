---
title: "طريقة Aspose::Words::Drawing::Stroke::get_Color2 method"
linktitle: "get_Color2"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Stroke::get_Color2. تحدد لونًا ثانيًا للخط في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing/stroke/get_color2/
---
## Stroke::get_Color2 method


يحدد لونًا ثانيًا للحد.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Stroke::get_Color2()
```

## ملاحظات


القيمة الافتراضية لـ [Shape](../../shape/) هي **White**.

## أمثلة



يوضح كيفية معالجة ميزات خط الشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();

// يمكن للخطوط أن تحتوي على لونين، يُستخدمان لإنشاء نمط يُحدد بواسطة بيانات صورة ذات لونين.
// الخطوط ذات اللون الواحد لا تستخدم الخاصية Color2.
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 128, 0, 0), stroke->get_Color());
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 255, 0), stroke->get_Color2());

ASSERT_FALSE(System::TestTools::IsNull(stroke->get_ImageBytes()));
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Drawing.StrokePattern.png", stroke->get_ImageBytes());
```

## انظر أيضًا

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
