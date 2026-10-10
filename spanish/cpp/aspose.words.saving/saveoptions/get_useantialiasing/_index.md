---
title: "Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing método"
linktitle: "get_UseAntiAliasing"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing método. Obtiene o establece un valor que determina si se debe usar o no anti-aliasing para el renderizado en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words.saving/saveoptions/get_useantialiasing/
---
## SaveOptions::get_UseAntiAliasing method


Obtiene o establece un valor que determina si se debe usar anti-aliasing para el renderizado.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing() const
```

## Observaciones


El valor predeterminado es **false**. Cuando este valor se establece en **true**, se utiliza anti-aliasing para el renderizado.

Esta propiedad se utiliza cuando el documento se exporta a los siguientes formatos: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/). Cuando el documento se exporta a los formatos [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) o [Mobi](../../../aspose.words/saveformat/), esta opción se utiliza para imágenes raster.

## Ejemplos



Muestra cómo mejorar la calidad de un documento renderizado con [SaveOptions](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```

## Ver también

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
