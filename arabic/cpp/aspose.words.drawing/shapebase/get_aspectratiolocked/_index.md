---
title: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked method"
linktitle: "get_AspectRatioLocked"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked method. يحدد ما إذا كانت نسبة أبعاد الشكل''s مقفلة في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.drawing/shapebase/get_aspectratiolocked/
---
## ShapeBase::get_AspectRatioLocked method


يحدد ما إذا كان نسبة أبعاد الشكل مقفلة.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked()
```

## ملاحظات


القيمة الافتراضية تعتمد على [ShapeType](../../shapetype/)، بالنسبة إلى [Image](../../shapetype/) تكون **true** ولكن بالنسبة لأنواع الأشكال الأخرى تكون **false**.

لها تأثير على الأشكال ذات المستوى الأعلى فقط.

## أمثلة



يظهر كيفية قفل/فتح نسبة أبعاد الشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج شكلاً. إذا فتحنا هذا المستند في Microsoft Word، يمكننا النقر بزر الفأرة الأيسر على الشكل للكشف عن
// ثمانية مقابض تحجيم حول محيطه، والتي يمكننا النقر والسحب لتغيير حجمه.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// اضبط الخاصية "AspectRatioLocked" إلى "true" للحفاظ على نسبة أبعاد الشكل
// عند استخدام أي من المقابض الأربعة القطرية للتحجيم، التي تغير كلًا من ارتفاع وعرض الصورة.
// استخدام أي مقابض تحجيم عمودية تغير إما الارتفاع أو العرض سيظل يغير نسبة الأبعاد.
// اضبط الخاصية "AspectRatioLocked" إلى "false" للسماح لنا بـ
// تغيير نسبة أبعاد الصورة بحرية باستخدام جميع مقابض التحجيم.
shape->set_AspectRatioLocked(lockAspectRatio);

doc->Save(get_ArtifactsDir() + u"Shape.AspectRatio.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
