---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_CoordOrigin"
linktitle: "get_CoordOrigin"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_CoordOrigin. الإحداثيات في الزاوية العلوية اليسرى للكتلة المحتوية لهذا الشكل في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.drawing/shapebase/get_coordorigin/
---
## ShapeBase::get_CoordOrigin method


الإحداثيات في الزاوية العلوية اليسرى للكتلة المحتوية على هذا الشكل.

```cpp
System::Drawing::Point Aspose::Words::Drawing::ShapeBase::get_CoordOrigin()
```

## ملاحظات


القيمة الافتراضية هي (0,0).

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
