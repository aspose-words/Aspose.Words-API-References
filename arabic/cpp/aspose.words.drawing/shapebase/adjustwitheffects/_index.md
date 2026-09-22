---
title: "طريقة Aspose::Words::Drawing::ShapeBase::AdjustWithEffects"
linktitle: "AdjustWithEffects"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::AdjustWithEffects. تُضيف إلى المستطيل المصدر قيم امتداد التأثير وتُعيد المستطيل النهائي في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.drawing/shapebase/adjustwitheffects/
---
## ShapeBase::AdjustWithEffects method


يضيف إلى المستطيل المصدر قيم مدى التأثير ويعيد المستطيل النهائي.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::AdjustWithEffects(System::Drawing::RectangleF source)
```


## أمثلة



يُظهر كيفية التحقق من كيفية تأثر حدود الشكل بتأثيرات الشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape shadow effect.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// الشكلان متطابقان من حيث الأبعاد ونوع الشكل.
ASPOSE_ASSERT_EQ(shapes[0]->get_Width(), shapes[1]->get_Width());
ASPOSE_ASSERT_EQ(shapes[0]->get_Height(), shapes[1]->get_Height());
ASSERT_EQ(shapes[0]->get_ShapeType(), shapes[1]->get_ShapeType());

// الشكل الأول لا يحتوي على تأثيرات، والثاني يحتوي على ظل وخط خارجي سميك.
// هذه التأثيرات تجعل حجم ظل الشكل الثاني أكبر من حجم الشكل الأول.
// على الرغم من أن حجم المستطيل يظهر عندما نضغط على هذه الأشكال في Microsoft Word،
// فإن الحدود الخارجية الظاهرة للشكل الثاني تتأثر بالظل والخط الخارجي وبالتالي تكون أكبر.
// يمكننا استخدام طريقة \"AdjustWithEffects\" لرؤية الحجم الحقيقي للشكل.
ASPOSE_ASSERT_EQ(0.0, shapes[0]->get_StrokeWeight());
ASPOSE_ASSERT_EQ(20.0, shapes[1]->get_StrokeWeight());
ASSERT_FALSE(shapes[0]->get_ShadowEnabled());
ASSERT_TRUE(shapes[1]->get_ShadowEnabled());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = shapes[0];

// إنشاء كائن RectangleF، يمثل مستطيلًا،
// والذي يمكننا استخدامه كإحداثيات وحدود لشكل.
System::Drawing::RectangleF rectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);

// شغّل هذه الطريقة للحصول على حجم المستطيل المعدل لجميع تأثيرات الشكل.
System::Drawing::RectangleF rectangleFOut = shape->AdjustWithEffects(rectangleF);

// نظرًا لعدم وجود تأثيرات تغير حدود الشكل، فإن أبعاد حدوده لا تتأثر.
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_Y());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Height());

// تحقق من الامتداد النهائي للشكل الأول بالنقاط.
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Height());

shape = shapes[1];
rectangleF = System::Drawing::RectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);
rectangleFOut = shape->AdjustWithEffects(rectangleF);

// لقد حركت تأثيرات الشكل الزاوية العليا اليسرى الظاهرة للشكل قليلاً.
ASPOSE_ASSERT_EQ(171.5, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(167, rectangleFOut.get_Y());

// كما أثرت التأثيرات على الأبعاد الظاهرة للشكل.
ASPOSE_ASSERT_EQ(1045, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1133.5, rectangleFOut.get_Height());

// كما أثرت التأثيرات على الحدود الظاهرة للشكل.
ASPOSE_ASSERT_EQ(-28.5, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(-33, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(192, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(280.5, shape->get_BoundsWithEffects().get_Height());
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
