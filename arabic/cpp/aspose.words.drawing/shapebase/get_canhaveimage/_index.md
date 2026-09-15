---
title: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage طريقة"
linktitle: "get_CanHaveImage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage طريقة. تُعيد **true** إذا كان نوع الشكل يسمح للشكل بامتلاك صورة في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.drawing/shapebase/get_canhaveimage/
---
## ShapeBase::get_CanHaveImage method


يرجع **true** إذا كان نوع الشكل يسمح بوجود صورة.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_CanHaveImage()
```

## ملاحظات


على الرغم من أن Microsoft Word يحتوي على نوع شكل خاص للصور، يبدو أنه في مستندات Microsoft Word يمكن لأي شكل باستثناء شكل مجموعة أن يحتوي على صورة، لذلك تُعيد هذه الخاصية **true** لجميع الأشكال باستثناء [GroupShape](../../groupshape/).

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
