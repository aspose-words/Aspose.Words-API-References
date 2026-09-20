---
title: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage método"
linktitle: "get_CanHaveImage"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage método. Devuelve **true** si el tipo de forma permite que la forma tenga una imagen en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.drawing/shapebase/get_canhaveimage/
---
## ShapeBase::get_CanHaveImage method


Devuelve **true** si el tipo de forma permite que la forma tenga una imagen.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_CanHaveImage()
```

## Observaciones


Aunque Microsoft Word tiene un tipo de forma especial para imágenes, parece que en los documentos de Microsoft Word cualquier forma, excepto una forma de grupo, puede tener una imagen; por lo tanto, esta propiedad devuelve **true** para todas las formas excepto [GroupShape](../../groupshape/).

## Ejemplos



Muestra cómo insertar y rotar una imagen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta una forma con una imagen.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// Rota la imagen 45 grados en sentido horario.
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
