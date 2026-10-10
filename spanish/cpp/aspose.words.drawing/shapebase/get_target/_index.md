---
title: "Aspose::Words::Drawing::ShapeBase::get_Target método"
linktitle: "get_Target"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Target método. Obtiene o establece el marco de destino para el hipervínculo de la forma en C++."
type: docs
weight: 50000
url: /es/cpp/aspose.words.drawing/shapebase/get_target/
---
## ShapeBase::get_Target method


Obtiene o establece el marco de destino para el hipervínculo de la forma.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Target()
```

## Observaciones


El valor predeterminado es una cadena vacía.

## Ejemplos



Muestra cómo insertar una forma que contiene una imagen y también es un hipervínculo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Ctrl + clic izquierdo en la forma en Microsoft Word abrirá una nueva ventana del navegador web
// y nos llevará al hipervínculo en la propiedad "HRef".
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
