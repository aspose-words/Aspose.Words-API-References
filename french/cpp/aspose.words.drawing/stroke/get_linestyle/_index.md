---
title: "Aspose::Words::Drawing::Stroke::get_LineStyle méthode"
linktitle: "get_LineStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Stroke::get_LineStyle méthode. Définit le style de ligne du trait en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.drawing/stroke/get_linestyle/
---
## Stroke::get_LineStyle method


Définit le style de ligne du trait.

```cpp
Aspose::Words::Drawing::ShapeLineStyle Aspose::Words::Drawing::Stroke::get_LineStyle()
```

## Remarques


La valeur par défaut est [Single](../../shapelinestyle/).

## Exemples



Montre comment modifier les propriétés du trait.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// Les formes de base, comme le rectangle, ont deux parties visibles.
// 1 -  Le remplissage, qui s'applique à la zone à l'intérieur du contour de la forme :
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  Le trait, qui délimite le contour de la forme :
// Modifiez diverses propriétés du trait de cette forme.
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

## Voir aussi

* Enum [ShapeLineStyle](../../shapelinestyle/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
