---
title: "Aspose::Words::Drawing::Stroke::get_Weight yöntemi"
linktitle: "get_Weight"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Stroke::get_Weight yöntemi. Bir şeklin yolunu çizen fırça kalınlığını puan cinsinden tanımlar (C++ içinde)."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.drawing/stroke/get_weight/
---
## Stroke::get_Weight method


Bir şeklin yolunu puan cinsinden çizen fırça kalınlığını tanımlar.

```cpp
double Aspose::Words::Drawing::Stroke::get_Weight()
```

## Açıklamalar


Bir [Shape](../../shape/) için varsayılan değer 0.75'tir.

## Örnekler



Vuruş özelliklerinin nasıl değiştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// Dikdörtgen gibi temel şekillerin iki görünür parçası vardır.
// 1 -  Doldurma, şeklin dış çizgisi içindeki alana uygulanır:
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  Vuruş, şeklin dış çizgisini işaretler:
// Bu şeklin vuruşunun çeşitli özelliklerini değiştirin.
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_On(true);
stroke->set_Weight(5);
stroke->set_Color(System::Drawing::Color::get_Red());
stroke->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDashDotDot);
stroke->set_JoinStyle(Aspose::Words::Drawing::JoinStyle::Miter);
stroke->set_EndCap(Aspose::Words::Drawing::EndCap::Square);
stroke->set_LineStyle(Aspose::Words::Drawing::ShapeLineStyle::Triple);
stroke->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Red(), System::Drawing::Color::get_Blue(), Aspose::Words::Drawing::GradientStyle::Vertical, Aspose::Words::Drawing::GradientVariant::Variant1);

doc->Save(get_ArtifactsDir() + u"Shape.Stroke.docx");
```

## Ayrıca Bakınız

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
