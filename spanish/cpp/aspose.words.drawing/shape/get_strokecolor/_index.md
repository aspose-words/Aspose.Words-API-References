---
title: "Método Aspose::Words::Drawing::Shape::get_StrokeColor"
linktitle: "get_StrokeColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Shape::get_StrokeColor. Define el color de un trazo en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words.drawing/shape/get_strokecolor/
---
## Shape::get_StrokeColor method


Define el color de un trazo.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Shape::get_StrokeColor()
```

## Observaciones


Este es un acceso directo a la propiedad [Color](../../stroke/get_color/).

El valor predeterminado es **Black**.

## Ejemplos



Muestra cómo rellenar una forma con un color sólido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Escribe algún texto y luego cúbrelo con una forma flotante.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Utiliza la propiedad "StrokeColor" para establecer el color del contorno de la forma.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Utiliza la propiedad "FillColor" para establecer el color del área interior de la forma.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// La propiedad "Opacity" determina cuán transparente es el color en una escala de 0 a 1,
// siendo 1 totalmente opaco y 0 invisible.
// El relleno de la forma por defecto es totalmente opaco, por lo que no podemos ver el texto que está debajo de esta forma.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Establezca la opacidad del color de relleno de la forma a un valor más bajo para que podamos ver el texto debajo de ella.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Ver también

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
