---
title: "Método Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution"
linktitle: "get_MaxImageResolution"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution. Obtiene o establece un valor en píxeles por pulgada que limita la resolución de las imágenes raster exportadas. El valor predeterminado es cero en C++."
type: docs
weight: 4500
url: /es/cpp/aspose.words.saving/svgsaveoptions/get_maximageresolution/
---
## SvgSaveOptions::get_MaxImageResolution method


Obtiene o establece un valor en píxeles por pulgada que limita la resolución de las imágenes raster exportadas. El valor predeterminado es cero.

```cpp
int32_t Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution() const
```

## Observaciones


Si el valor de esta propiedad no es cero, limita la resolución de las imágenes raster exportadas. Es decir, las imágenes de mayor resolución se remuestrean hacia abajo al límite y las imágenes de menor resolución se exportan tal cual.

Si el valor de esta propiedad es cero, todas las imágenes raster se exportan sin remuestreo.

## Ejemplos



Muestra cómo establecer un límite para la resolución de imágenes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Ver también

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
