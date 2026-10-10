---
title: "Aspose::Words::Drawing::Stroke::get_On metodo"
linktitle: "get_On"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Stroke::get_On metodo. Definisce se il percorso sarà tracciato in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.drawing/stroke/get_on/
---
## Stroke::get_On method


Definisce se il percorso sarà tracciato.

```cpp
bool Aspose::Words::Drawing::Stroke::get_On()
```

## Note


Il valore predefinito per un [Shape](../../shape/) è **true**.

## Esempi



Mostra come modificare le proprietà del tratto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// Le forme di base, come il rettangolo, hanno due parti visibili.
// 1 -  Il riempimento, che si applica all'area all'interno del contorno della forma:
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  Il tratto, che segna il contorno della forma:
// Modifica varie proprietà del tratto di questa forma.
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

## Vedi anche

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
