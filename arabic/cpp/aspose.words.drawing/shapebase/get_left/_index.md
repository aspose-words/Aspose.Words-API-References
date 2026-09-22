---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_Left"
linktitle: "get_Left"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_Left. تحصل أو تعين موضع الحافة اليسرى للكتلة التي تحتوي الشكل في C++."
type: docs
weight: 38000
url: /ar/cpp/aspose.words.drawing/shapebase/get_left/
---
## ShapeBase::get_Left method


الحصول أو تعيين موضع الحافة اليسرى للكتلة المحتوية على الشكل.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Left()
```

## ملاحظات


بالنسبة لشكل من المستوى الأعلى، تكون القيمة بالنقاط ومقارنة بمرساة الشكل.

بالنسبة للأشكال داخل مجموعة، تكون القيمة في مساحة الإحداثيات ووحدات المجموعة الأصلية.

القيمة الافتراضية هي 0.

يؤثر فقط على الأشكال العائمة.

## أمثلة



يُظهر كيفية إدراج صورة عائمة، وتحديد موضعها وحجمها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// قم بتكوين خاصية "RelativeHorizontalPosition" للشكل لتعامل مع قيمة خاصية "Left"
// كالمسافة الأفقية للشكل، بالنقاط، من الجانب الأيسر للصفحة.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// عيّن المسافة الأفقية للشكل من الجانب الأيسر للصفحة إلى 100.
shape->set_Left(100);

// استخدم خاصية "RelativeVerticalPosition" بطريقة مماثلة لتحديد موضع الشكل 80 نقطة أسفل أعلى الصفحة.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// عيّن ارتفاع الشكل، والذي سيُعيد تحجيم العرض تلقائيًا للحفاظ على الأبعاد.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// خاصيتي "Bottom" و "Right" تحتويان على الحافة السفلية واليمنى للصورة.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
