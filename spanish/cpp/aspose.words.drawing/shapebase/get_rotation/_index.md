---
title: "Aspose::Words::Drawing::ShapeBase::get_Rotation método"
linktitle: "get_Rotation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Rotation método. Define el ángulo (en grados) con el que se rota una forma. Un valor positivo corresponde al ángulo de rotación en sentido horario en C++."
type: docs
weight: 45000
url: /es/cpp/aspose.words.drawing/shapebase/get_rotation/
---
## ShapeBase::get_Rotation method


Define el ángulo (en grados) al que se rota una forma. Un valor positivo corresponde al ángulo de rotación en sentido horario.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Rotation()
```

## Observaciones


El valor predeterminado es 0.

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
