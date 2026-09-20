---
title: "Método Aspose::Words::Drawing::ShapeBase::get_AlternativeText"
linktitle: "get_AlternativeText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShapeBase::get_AlternativeText. Define el texto alternativo que se mostrará en lugar de un gráfico en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.drawing/shapebase/get_alternativetext/
---
## ShapeBase::get_AlternativeText method


Define el texto alternativo que se mostrará en lugar de un gráfico.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_AlternativeText()
```

## Observaciones


El valor predeterminado es una cadena vacía.

## Ejemplos



Muestra cómo usar el texto alternativo de una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 150, 150);
shape->set_Name(u"MyCube");

shape->set_AlternativeText(u"Alt text for MyCube.");

// Podemos acceder al texto alternativo de una forma haciendo clic derecho sobre ella y luego mediante "Format AutoShape" -> "Alt Text".
doc->Save(get_ArtifactsDir() + u"Shape.AltText.docx");

// Guarde el documento en HTML y luego elimine la imagen vinculada que pertenece a nuestra forma.
// El navegador que está leyendo nuestro HTML mostrará el texto alternativo en lugar de la imagen faltante.
doc->Save(get_ArtifactsDir() + u"Shape.AltText.html");
System::IO::File::Delete(get_ArtifactsDir() + u"Shape.AltText.001.png");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
