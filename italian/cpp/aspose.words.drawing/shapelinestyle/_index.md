---
title: "Aspose::Words::Drawing::ShapeLineStyle enum"
linktitle: "ShapeLineStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeLineStyle enum. Specifica lo stile di linea composto di una Shape in C++."
type: docs
weight: 36000
url: /it/cpp/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enum


Specifica lo stile di linea composto di un [Shape](../shape/).

```cpp
enum class ShapeLineStyle
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Singola | 0 | Linea singola. |
| Doppia | 1 | Doppie linee di uguale larghezza. |
| ThickThin | 2 | Doppie linee, una spessa, una sottile. |
| ThinThick | 3 | Doppie linee, una sottile, una spessa. |
| Triple | 4 | Tre linee, sottile, spessa, sottile. |
| Default | n/a | Il valore predefinito è [Single](./). |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
