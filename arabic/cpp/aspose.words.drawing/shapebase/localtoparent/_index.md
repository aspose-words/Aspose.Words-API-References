---
title: "طريقة Aspose::Words::Drawing::ShapeBase::LocalToParent"
linktitle: "LocalToParent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::LocalToParent. يحول قيمة من مساحة الإحداثيات المحلية إلى مساحة إحداثيات الشكل الأب في C++."
type: docs
weight: 61000
url: /ar/cpp/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase::LocalToParent method


يحوّل قيمة من مساحة الإحداثيات المحلية إلى مساحة إحداثيات الشكل الأب.

```cpp
System::Drawing::PointF Aspose::Words::Drawing::ShapeBase::LocalToParent(System::Drawing::PointF value)
```


## أمثلة



يوضح كيفية تحويل موقع إحداثيات x و y على مستوى إحداثيات الشكل إلى موقع على مستوى إحداثيات الشكل الأب.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أدرج شكل مجموعة، وضعه 100 نقطة أسفل وإلى يمين
// نقطة أصل إحداثيات x و Y للوثيقة.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 100.0f, 500.0f, 500.0f));

// استخدم طريقة \"LocalToParent\" لتحديد أن (0, 0) على إحداثيات x و y الداخلية للمجموعة
// تقع على (100, 100) في نظام إحداثيات الشكل الأب. أصل شكل المجموعة هو الوثيقة نفسها.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(100.0f, 100.0f), group->LocalToParent(System::Drawing::PointF(0.0f, 0.0f)));

// بشكل افتراضي، يكون مستوى إحداثيات الشكل الداخلي له الزاوية العلوية اليسرى عند (0, 0)،
// والزاوية السفلية اليمنى عند (1000, 1000). بسبب حجمه، يغطي شكل مجموعتنا مساحة 500pt × 500pt
// في مستوى الوثيقة. هذا يعني أن حركة 1pt على مستوى إحداثيات الوثيقة ستحول
// إلى حركة 2pt على مستوى إحداثيات شكل المجموعة.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(150.0f, 150.0f), group->LocalToParent(System::Drawing::PointF(100.0f, 100.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(200.0f, 200.0f), group->LocalToParent(System::Drawing::PointF(200.0f, 200.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(250.0f, 250.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// حرك أصل محور x و y لشكل المجموعة من الزاوية العلوية اليسرى إلى المركز.
// سيؤدي ذلك إلى إزاحة إحداثيات المجموعة الداخلية بالنسبة لإحداثيات المستند بشكل أكبر.
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(375.0f, 375.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// تغيير مقياس مستوى الإحداثيات سيؤثر أيضًا على المواقع النسبية.
group->set_CoordSize(System::Drawing::Size(500, 500));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(650.0f, 650.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// إذا رغبنا في إضافة شكل إلى هذه المجموعة مع تحديد موقعه بناءً على موقع في المستند،
// سنحتاج أولاً إلى تأكيد موقع في شكل المجموعة يتطابق مع موقع المستند.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(700.0f, 700.0f), group->LocalToParent(System::Drawing::PointF(350.0f, 350.0f)));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

doc->Save(get_ArtifactsDir() + u"Shape.LocalToParent.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
