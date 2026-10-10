---
title: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked método"
linktitle: "get_AspectRatioLocked"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked método. Especifica si la relación de aspecto de la forma está bloqueada en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.drawing/shapebase/get_aspectratiolocked/
---
## ShapeBase::get_AspectRatioLocked method


Especifica si la relación de aspecto de la forma está bloqueada.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked()
```

## Observaciones


El valor predeterminado depende del [ShapeType](../../shapetype/), para el [Image](../../shapetype/) es **true** pero para los otros tipos de forma es **false**.

Tiene efecto solo para formas de nivel superior.

## Ejemplos



Muestra cómo bloquear/desbloquear la relación de aspecto de una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una forma. Si abrimos este documento en Microsoft Word, podemos hacer clic izquierdo en la forma para revelar
// ocho controladores de tamaño alrededor de su perímetro, que podemos hacer clic y arrastrar para cambiar su tamaño.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Establezca la propiedad "AspectRatioLocked" a "true" para preservar la relación de aspecto de la forma
// al usar cualquiera de los cuatro controladores de tamaño diagonales, que cambian tanto la altura como el ancho de la imagen.
// Usar cualquier controlador de tamaño ortogonal que cambie la altura o el ancho aún modificará la relación de aspecto.
// Establezca la propiedad "AspectRatioLocked" a "false" para permitirnos
// cambiar libremente la relación de aspecto de la imagen con todos los controladores de tamaño.
shape->set_AspectRatioLocked(lockAspectRatio);

doc->Save(get_ArtifactsDir() + u"Shape.AspectRatio.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
