---
title: "Aspose::Words::Drawing::ShapeLineStyle enum"
linktitle: "ShapeLineStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeLineStyle enum. Especifica el estilo de línea compuesto de una Shape en C++."
type: docs
weight: 36000
url: /es/cpp/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enum


Especifica el estilo de línea compuesta de una [Shape](../shape/).

```cpp
enum class ShapeLineStyle
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Single | 0 | Línea simple. |
| Double | 1 | Doble líneas de igual ancho. |
| ThickThin | 2 | Doble líneas, una gruesa, una delgada. |
| ThinThick | 3 | Doble líneas, una delgada, una gruesa. |
| Triple | 4 | Tres líneas, delgada, gruesa, delgada. |
| Default | n/a | El valor predeterminado es [Single](./). |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
