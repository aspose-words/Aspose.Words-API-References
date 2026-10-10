---
title: "Aspose::Words::Drawing::ShapeBase::get_Bounds طريقة"
linktitle: "get_Bounds"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Bounds طريقة. يحصل على أو يضبط موقع وحجم كتلة الحاوية للشكل في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.drawing/shapebase/get_bounds/
---
## ShapeBase::get_Bounds method


يحصل أو يضبط موقع وحجم الكتلة المحتوية على الشكل.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_Bounds()
```

## ملاحظات


يتجاهل قفل نسبة الأبعاد عند الضبط.

بالنسبة لشكل من المستوى الأعلى، تكون القيمة بالنقاط ومقارنة بمرساة الشكل.

بالنسبة للأشكال داخل مجموعة، تكون القيمة في مساحة الإحداثيات ووحدات المجموعة الأصلية.

## أمثلة



يوضح كيفية إنشاء وتعبئة شكل مجموعة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// إنشاء شكل مجموعة. يمكن لِشكل المجموعة عرض مجموعة من عقد الأشكال الفرعية.
// في Microsoft Word، النقر داخل حدود شكل المجموعة أو على أحد الأشكال الفرعية لِشكل المجموعة سيؤدي إلى
// تحديد جميع الأشكال الفرعية الأخرى داخل هذه المجموعة والسماح لنا بتكبير وتحريك جميع الأشكال مرة واحدة.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);

ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, group->get_WrapType());

// إنشاء شكل مجموعة بحجم 400pt × 400pt ووضعه عند أصل إحداثيات الشكل العائم في المستند.
group->set_Bounds(System::Drawing::RectangleF(0.0f, 0.0f, 400.0f, 400.0f));

// قم بتعيين حجم طائرة الإحداثيات الداخلية للمجموعة إلى 500 × 500pt.
// الزاوية العلوية اليسرى للمجموعة سيكون لها إحداثي x و y قيمته (0, 0)،
// والزاوية السفلية اليمنى سيكون لها إحداثي x و y قيمته (500, 500).
group->set_CoordSize(System::Drawing::Size(500, 500));

// اضبط إحداثيات الزاوية العلوية اليسرى للمجموعة إلى (-250, -250).
// مركز المجموعة سيصبح الآن له إحداثي x و y قيمته (0, 0)،
// والزاوية السفلية اليمنى ستكون عند (250, 250).
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

// أنشئ مستطيلًا سيعرض حدود شكل المجموعة هذا وأضفه إلى المجموعة.
auto child1 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child1->set_Width(group->get_CoordSize().get_Width());
child1->set_Height(group->get_CoordSize().get_Height());
child1->set_Left(group->get_CoordOrigin().get_X());
child1->set_Top(group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child1);

// بمجرد أن يصبح الشكل جزءًا من شكل مجموعة، يمكننا الوصول إليه كعقدة فرعية ثم تعديلها.
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::Dash);

// أنشئ نجمة حمراء صغيرة وأدرجها في المجموعة.
// حاذِ الشكل مع أصل إحداثيات المجموعة، الذي نقلناه إلى المركز.
auto child2 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Star);
child2->set_Width(20);
child2->set_Height(20);
child2->set_Left(-10);
child2->set_Top(-10);
child2->set_FillColor(System::Drawing::Color::get_Red());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child2);

// أدرج مستطيلًا، ثم أدخل مستطيلًا أصغر قليلًا في نفس المكان مع صورة.
// الأشكال الأحدث التي نضيفها إلى المجموعة تتداخل مع الأشكال القديمة. المستطيل الأزرق الفاتح سيتداخل جزئيًا مع النجمة الحمراء،
// ثم الشكل الذي يحتوي على الصورة سيتداخل مع المستطيل الأزرق الفاتح، مستخدمًا إياه كإطار.
// لا يمكننا استخدام خصائص \"ZOrder\" للأشكال لتعديل ترتيبها داخل شكل مجموعة.
auto child3 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child3->set_Width(250);
child3->set_Height(250);
child3->set_Left(-250);
child3->set_Top(-250);
child3->set_FillColor(System::Drawing::Color::get_LightBlue());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child3);

auto child4 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
child4->set_Width(200);
child4->set_Height(200);
child4->set_Left(-225);
child4->set_Top(-225);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child4);

(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 3, true)))->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// أدرج صندوق نص داخل شكل المجموعة. اضبط خاصية \"Left\" بحيث يكون الحافة اليمنى لصندوق النص
// تلامس الحد الأيمن لشكل المجموعة. اضبط خاصية \"Top\" بحيث يكون صندوق النص خارج
// حدود شكل المجموعة، مع محاذاة الجزء العلوي له على الهامش السفلي لشكل المجموعة.
auto child5 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
child5->set_Width(200);
child5->set_Height(50);
child5->set_Left(group->get_CoordSize().get_Width() + group->get_CoordOrigin().get_X() - 200);
child5->set_Top(group->get_CoordSize().get_Height() + group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child5);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(group);
builder->MoveTo((System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 4, true)))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Shape.GroupShape.docx");
```


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
