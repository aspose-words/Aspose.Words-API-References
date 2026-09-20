---
title: "Método Aspose::Words::Drawing::Fill::get_Opacity"
linktitle: "get_Opacity"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Fill::get_Opacity. Obtiene o establece el grado de opacidad del relleno especificado como un valor entre 0.0 (transparente) y 1.0 (opaco) en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.drawing/fill/get_opacity/
---
## Fill::get_Opacity method


Obtiene o establece el grado de opacidad del relleno especificado como un valor entre 0.0 (transparente) y 1.0 (opaco).

```cpp
double Aspose::Words::Drawing::Fill::get_Opacity()
```


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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
