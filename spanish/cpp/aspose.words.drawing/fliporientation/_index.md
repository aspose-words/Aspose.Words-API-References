---
title: "Aspose::Words::Drawing::FlipOrientation enum"
linktitle: "FlipOrientation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::FlipOrientation enum. Valores posibles para la orientación de una forma en C++."
type: docs
weight: 23000
url: /es/cpp/aspose.words.drawing/fliporientation/
---
## FlipOrientation enum


Valores posibles para la orientación de una forma.

```cpp
enum class FlipOrientation
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | Las coordenadas no están invertidas. |
| Horizontal | 1 | Voltear a lo largo del eje y, invirtiendo las coordenadas x. |
| Vertical | 2 | Voltear a lo largo del eje x, invirtiendo las coordenadas y. |
| Both | 3 | Voltear a lo largo de los ejes y y x. |


## Ejemplos



Muestra cómo voltear una forma en un eje.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una forma de imagen y mantenga su orientación en su estado predeterminado.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::FlipOrientation::None, shape->get_FlipOrientation());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Establezca la propiedad \"FlipOrientation\" a \"FlipOrientation.Horizontal\" para voltear la segunda forma en el eje y,
// convirtiéndola en una imagen espejo horizontal de la primera forma.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Horizontal);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Establezca la propiedad \"FlipOrientation\" a \"FlipOrientation.Horizontal\" para voltear la tercera forma en el eje x,
// convirtiéndola en una imagen espejo vertical de la primera forma.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Vertical);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Establezca la propiedad \"FlipOrientation\" a \"FlipOrientation.Horizontal\" para voltear la cuarta forma en ambos ejes x e y,
// convirtiéndola en una imagen espejo horizontal y vertical de la primera forma.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Both);

doc->Save(get_ArtifactsDir() + u"Shape.FlipShapeOrientation.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
