---
title: "Aspose::Words::DocumentBuilder::InsertGroupShape yöntemi"
linktitle: "InsertGroupShape"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertGroupShape yöntemi. Parametre olarak verilen şekilleri yeni bir GroupShape düğümüne gruplar ve bu düğüm C++'da geçerli konuma eklenir."
type: docs
weight: 35500
url: /tr/cpp/aspose.words/documentbuilder/insertgroupshape/
---
## DocumentBuilder::InsertGroupShape(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


Parametre olarak verilen şekilleri yeni bir GroupShape düğümüne gruplar ve bu düğüm geçerli konuma eklenir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| şekiller | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | Gruplanacak şekillerin listesi. |
## Açıklamalar


Yeni GroupShape'in konumu ve boyutu otomatik olarak hesaplanacaktır.

VML ve DML şekilleri birlikte gruplanamaz.

## Örnekler



DML grup şeklinin nasıl ekleneceğini gösterir.
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

// Yeni GroupShape düğümünün boyutları.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Belirtilen boyutta GroupShape düğümünü ekler; bu düğüm belirtilen konuma yerleştirilir.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(left, top, width, height, System::ExplicitCast<System::Array<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>>(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Shape>>({shape1, shape2})));

// Konumu ve boyutu otomatik olarak hesaplanacak GroupShape düğümünü ekle.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.InsertGroupShape.docx");
```


Grup şekli ile şekli nasıl birleştireceğini gösterir.
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

// Şekilleri belirtilen konuma eklenen bir GroupShape düğümüne birleştir.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape1, shape2}));

// Shape ve GroupShape düğümlerini birleştir.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({groupShape1, shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.CombineGroupShape.docx");
```

## Ayrıca Bakınız

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertGroupShape(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


Parametre olarak verilen şekilleri belirtilen boyutta yeni bir GroupShape düğümüne gruplar ve bu düğüm belirtilen konuma eklenir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(double left, double top, double width, double height, const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| left | double | Orijinden grup şeklinin sol tarafına olan mesafe (puan cinsinden). |
| üst | double | Orijinden grup şeklinin üst tarafına olan mesafe (puan cinsinden). |
| genişlik | double | Grup şeklinin genişliği puan cinsindendir. Negatif bir değer kabul edilmez. |
| yükseklik | double | Grup şeklinin yüksekliği puan cinsindendir. Negatif bir değer kabul edilmez. |
| şekiller | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | Gruplanacak şekillerin listesi. |

## Örnekler



DML grup şeklinin nasıl ekleneceğini gösterir.
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

// Yeni GroupShape düğümünün boyutları.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Belirtilen boyutta GroupShape düğümünü ekler; bu düğüm belirtilen konuma yerleştirilir.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(left, top, width, height, System::ExplicitCast<System::Array<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>>(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Shape>>({shape1, shape2})));

// Konumu ve boyutu otomatik olarak hesaplanacak GroupShape düğümünü ekle.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.InsertGroupShape.docx");
```

## Ayrıca Bakınız

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
