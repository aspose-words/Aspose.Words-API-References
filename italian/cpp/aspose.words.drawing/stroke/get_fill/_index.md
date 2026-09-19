---
title: "Aspose::Words::Drawing::Stroke::get_Fill metodo"
linktitle: "get_Fill"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Stroke::get_Fill metodo. Ottiene la formattazione di riempimento per lo Stroke in C++."
type: docs
weight: 9500
url: /it/cpp/aspose.words.drawing/stroke/get_fill/
---
## Stroke::get_Fill method


Ottiene la formattazione di riempimento per il [Stroke](../).

```cpp
System::SharedPtr<Aspose::Words::Drawing::Fill> Aspose::Words::Drawing::Stroke::get_Fill()
```


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

* Class [Fill](../../fill/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
