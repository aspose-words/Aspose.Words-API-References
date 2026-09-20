---
title: "Método Aspose::Words::Drawing::Stroke::get_Fill"
linktitle: "get_Fill"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Stroke::get_Fill. Obtiene el formato de relleno para el Stroke en C++."
type: docs
weight: 9500
url: /es/cpp/aspose.words.drawing/stroke/get_fill/
---
## Stroke::get_Fill method


Obtiene el formato de relleno para el [Stroke](../).

```cpp
System::SharedPtr<Aspose::Words::Drawing::Fill> Aspose::Words::Drawing::Stroke::get_Fill()
```


## Ejemplos



Muestra cómo cambiar las propiedades del trazo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// Las formas básicas, como el rectángulo, tienen dos partes visibles.
// 1 -  El relleno, que se aplica al área dentro del contorno de la forma:
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  El trazo, que marca el contorno de la forma:
// Modifique varias propiedades del trazo de esta forma.
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

## Ver también

* Class [Fill](../../fill/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
