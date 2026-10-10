---
title: "طريقة Aspose::Words::DocumentBuilder::InsertGroupShape"
linktitle: "InsertGroupShape"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertGroupShape. تقوم بتجميع الأشكال الممررة كمعامل في عقدة GroupShape جديدة يتم إدراجها في الموضع الحالي في C++."
type: docs
weight: 35500
url: /ar/cpp/aspose.words/documentbuilder/insertgroupshape/
---
## DocumentBuilder::InsertGroupShape(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


يجمع الأشكال الممررة كمعامل في عقدة GroupShape جديدة تُدرج في الموضع الحالي.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| الأشكال | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | قائمة الأشكال التي سيتم تجميعها. |
## ملاحظات


سيتم حساب موضع وأبعاد الـ GroupShape الجديد تلقائيًا.

لا يمكن تجميع أشكال VML و DML معًا.

## أمثلة



يوضح كيفية إدراج شكل مجموعة DML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape1 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 250);
shape1->set_Left(20);
shape1->set_Top(20);
shape1->get_Stroke()->set_Color(System::Drawing::Color::get_Red());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape2 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 150, 200);
shape2->set_Left(40);
shape2->set_Top(50);
shape2->get_Stroke()->set_Color(System::Drawing::Color::get_Green());

// الأبعاد لعقدة GroupShape الجديدة.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// إدراج عقدة GroupShape بالحجم المحدد والتي يتم إدراجها في الموضع المحدد.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(left, top, width, height, System::ExplicitCast<System::Array<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>>(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Shape>>({shape1, shape2})));

// إدراج عقدة GroupShape التي سيتم حساب موضعها وأبعادها تلقائيًا.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.InsertGroupShape.docx");
```


يوضح كيفية دمج شكل المجموعة مع الشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape1 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 250);
shape1->set_Left(20);
shape1->set_Top(20);
shape1->get_Stroke()->set_Color(System::Drawing::Color::get_Red());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape2 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 150, 200);
shape2->set_Left(40);
shape2->set_Top(50);
shape2->get_Stroke()->set_Color(System::Drawing::Color::get_Green());

// دمج الأشكال في عقدة GroupShape يتم إدراجها في الموضع المحدد.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape1, shape2}));

// دمج عقدة Shape وعقدة GroupShape.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({groupShape1, shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.CombineGroupShape.docx");
```

## انظر أيضًا

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertGroupShape(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


يجمع الأشكال الممررة كمعامل في عقدة GroupShape جديدة بالحجم المحدد تُدرج في الموضع المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(double left, double top, double width, double height, const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| left | double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من شكل المجموعة. |
| top | double | المسافة بالنقاط من الأصل إلى الجانب العلوي من شكل المجموعة. |
| العرض | double | عرض شكل المجموعة بالنقاط. لا يُسمح بالقيمة السالبة. |
| الارتفاع | double | ارتفاع شكل المجموعة بالنقاط. لا يُسمح بالقيمة السالبة. |
| الأشكال | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | قائمة الأشكال التي سيتم تجميعها. |

## أمثلة



يوضح كيفية إدراج شكل مجموعة DML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape1 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 250);
shape1->set_Left(20);
shape1->set_Top(20);
shape1->get_Stroke()->set_Color(System::Drawing::Color::get_Red());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape2 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 150, 200);
shape2->set_Left(40);
shape2->set_Top(50);
shape2->get_Stroke()->set_Color(System::Drawing::Color::get_Green());

// الأبعاد لعقدة GroupShape الجديدة.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// إدراج عقدة GroupShape بالحجم المحدد والتي يتم إدراجها في الموضع المحدد.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(left, top, width, height, System::ExplicitCast<System::Array<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>>(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Shape>>({shape1, shape2})));

// إدراج عقدة GroupShape التي سيتم حساب موضعها وأبعادها تلقائيًا.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.InsertGroupShape.docx");
```

## انظر أيضًا

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
