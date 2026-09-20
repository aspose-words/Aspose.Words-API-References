---
title: "Aspose::Words::DocumentBase::get_PageColor método"
linktitle: "get_PageColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBase::get_PageColor método. Obtiene o establece el color de página del documento. Esta propiedad es una versión más simple de BackgroundShape en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/documentbase/get_pagecolor/
---
## DocumentBase::get_PageColor method


Obtiene o establece el color de página del documento. Esta propiedad es una versión más simple de [BackgroundShape](../get_backgroundshape/).

```cpp
System::Drawing::Color Aspose::Words::DocumentBase::get_PageColor()
```

## Observaciones


Esta propiedad proporciona una manera sencilla de especificar un color de página sólido para el documento. Establecer esta propiedad crea y asigna una [BackgroundShape](../get_backgroundshape/) apropiada.

Si el color de página no está establecido (p. ej., no hay forma de fondo en el documento) devuelve **Empty**.

## Ejemplos



Muestra cómo establecer el color de fondo para todas las páginas de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->set_PageColor(System::Drawing::Color::get_LightGray());

doc->Save(get_ArtifactsDir() + u"DocumentBase.SetPageColor.docx");
```

## Ver también

* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
