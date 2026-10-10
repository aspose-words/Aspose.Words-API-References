---
title: "Método Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode"
linktitle: "get_ImlRenderingMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode. Obtiene o establece un valor que determina cómo se renderizan los objetos de tinta (InkML) en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.saving/saveoptions/get_imlrenderingmode/
---
## SaveOptions::get_ImlRenderingMode method


Obtiene o establece un valor que determina cómo se renderizan los objetos de tinta (InkML).

```cpp
Aspose::Words::Saving::ImlRenderingMode Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode() const
```

## Observaciones


El valor predeterminado es [InkML](../../imlrenderingmode/).

Esta propiedad se utiliza cuando el documento se exporta a formatos de página fija.

## Ejemplos



Muestra cómo renderizar el objeto Ink.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Ink object.docx");

// Establezca 'ImlRenderingMode.InkML' para que ignore la forma de respaldo del objeto de tinta (InkML) y renderice InkML directamente.
// Si el resultado del renderizado es insatisfactorio,
// por favor use 'ImlRenderingMode.Fallback' para obtener un resultado similar a versiones anteriores.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(Aspose::Words::Saving::ImlRenderingMode::InkML);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## Ver también

* Enum [ImlRenderingMode](../../imlrenderingmode/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
