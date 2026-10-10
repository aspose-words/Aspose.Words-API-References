---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream método"
linktitle: "get_ImageStream"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream método. Permite especificar el flujo donde se guardará la imagen en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/imagesavingargs/get_imagestream/
---
## ImageSavingArgs::get_ImageStream method


Permite especificar el flujo donde se guardará la imagen.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ImageSavingArgs::get_ImageStream() const
```

## Observaciones


Esta propiedad le permite guardar imágenes en flujos en lugar de archivos durante HTML.

El valor predeterminado es **null**. Cuando esta propiedad es **null**, la imagen se guardará en un archivo especificado en la propiedad [ImageFileName](../get_imagefilename/).

Usando [IImageSavingCallback](../../iimagesavingcallback/) no puede sustituir una imagen por otra. Está destinado solo al control sobre la ubicación donde guardar las imágenes.

## Ver también

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
