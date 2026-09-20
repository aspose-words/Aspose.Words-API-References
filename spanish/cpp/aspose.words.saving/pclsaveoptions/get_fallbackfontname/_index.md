---
title: "Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName método"
linktitle: "get_FallbackFontName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName método. Nombre de la fuente que se utilizará si no se encuentra la fuente esperada en la impresora y en las colecciones de fuentes incorporadas en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/pclsaveoptions/get_fallbackfontname/
---
## PclSaveOptions::get_FallbackFontName method


Nombre de la fuente que se utilizará si no se encuentra la fuente esperada en la impresora y en las colecciones de fuentes integradas.

```cpp
System::String Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName() const
```


## Ejemplos



Muestra cómo declarar una fuente que la impresora aplicará al texto impreso como sustituto si su fuente original no está disponible.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_FallbackFontName(u"Times New Roman");

// Este documento instruirá a la impresora a aplicar "Times New Roman" al texto con la fuente faltante.
// Si "Times New Roman" también no está disponible, la impresora usará por defecto la fuente "Arial".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

## Ver también

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
