---
title: "Método Aspose::Words::Drawing::ShapeBase::get_HRef"
linktitle: "get_HRef"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShapeBase::get_HRef. Obtiene o establece la dirección completa del hipervínculo para una forma en C++."
type: docs
weight: 24000
url: /es/cpp/aspose.words.drawing/shapebase/get_href/
---
## ShapeBase::get_HRef method


Obtiene o establece la dirección completa del hipervínculo para una forma.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_HRef()
```

## Observaciones


El valor predeterminado es una cadena vacía.

A continuación se presentan ejemplos de valores válidos para esta propiedad:

URI completa: **https://www.aspose.com/**.

Nombre de archivo completo: **C:\\My Documents\\SalesReport.doc**.

URI relativa: **%../../../resource.txt**

Nombre de archivo relativo: **%..\\My Documents\\SalesReport.doc**.

[Bookmark](../../../aspose.words/bookmark/) within another document: **https://www.aspose.com/Products/Default.aspx::Suites**

[Bookmark](../../../aspose.words/bookmark/) within this document: **%#BookmakName**.

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
