---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_Rotation"
linktitle: "get_Rotation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_Rotation. يحدد الزاوية (بالدرجات) التي يتم تدوير الشكل بها. القيمة الموجبة تمثل زاوية التدوير في اتجاه عقارب الساعة في C++."
type: docs
weight: 45000
url: /ar/cpp/aspose.words.drawing/shapebase/get_rotation/
---
## ShapeBase::get_Rotation method


يحدد الزاوية (بالدرجات) التي يتم تدوير الشكل بها. القيمة الإيجابية تتطابق مع زاوية الدوران في اتجاه عقارب الساعة.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Rotation()
```

## ملاحظات


القيمة الافتراضية هي 0.

## أمثلة



يعرض كيفية إدراج وتدوير صورة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج شكلاً مع صورة.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// دوّر الصورة 45 درجة باتجاه عقارب الساعة.
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
