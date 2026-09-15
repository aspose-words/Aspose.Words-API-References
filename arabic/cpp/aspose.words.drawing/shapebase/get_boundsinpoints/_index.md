---
title: "Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints method"
linktitle: "get_BoundsInPoints"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints method. يحصل على موقع وحجم كتلة الحاوية للشكل بالنقاط، بالنسبة إلى مرساة الشكل الأعلى في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.drawing/shapebase/get_boundsinpoints/
---
## ShapeBase::get_BoundsInPoints method


يحصل على موقع وحجم الكتلة المحتوية على الشكل بالنقاط، بالنسبة إلى مرساة الشكل الأعلى.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints()
```


## أمثلة



يظهر كيفية التحقق من حدود كتلة الحاوية للشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Line, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 50, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_StrokeColor(System::Drawing::Color::get_Orange());

// على الرغم من أن السطر نفسه يشغل مساحة قليلة على صفحة المستند،
// إلا أنه يشغل كتلة حاوية مستطيلة، يمكننا تحديد حجمها باستخدام خصائص "Bounds".
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_Bounds());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

// أنشئ شكل مجموعة، ثم اضبط حجم كتلة الحاوية الخاصة به باستخدام خاصية "Bounds".
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f));

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());

// أنشئ مستطيلًا، تحقق من حجم كتلته الحدودية، ثم أضفه إلى شكل المجموعة.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(700.0f, 700.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// محور إحداثيات شكل المجموعة له أصله في الزاوية العلوية اليسرى لكتلة الحاوية الخاصة به،
// والإحداثيات x و y للنقطة (1000, 1000) في الزاوية السفلية اليمنى.
// حجم شكل مجموعتنا هو 250×250pt، لذا كل 4pt على محور إحداثيات شكل المجموعة
// يعادل 1pt في محور إحداثيات جسم المستند.
// كل شكل نقوم بإدراجه سيتقلص أيضًا في الحجم بمعامل 4.
// سيعكس التغيير في خاصية "BoundsInPoints" للشكل ذلك.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(175.0f, 275.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

// أدرج شكلًا وضعه خارج حدود كتلة الحاوية لشكل المجموعة.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(1000);
shape->set_Top(1000);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// زادت البصمة الخاصة بشكل المجموعة في جسم المستند، لكن كتلة الحاوية تظل كما هي.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(250.0f, 350.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->Save(get_ArtifactsDir() + u"Shape.Bounds.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
