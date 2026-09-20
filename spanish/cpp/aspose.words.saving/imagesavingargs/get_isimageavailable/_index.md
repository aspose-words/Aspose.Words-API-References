---
title: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable método"
linktitle: "get_IsImageAvailable"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable método. Devuelve true si la imagen actual está disponible para exportar en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.saving/imagesavingargs/get_isimageavailable/
---
## ImageSavingArgs::get_IsImageAvailable method


Devuelve **true** si la imagen actual está disponible para exportar.

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable() const
```

## Observaciones


Algunas imágenes en el documento pueden no estar disponibles, por ejemplo, porque la imagen está vinculada y el enlace es inaccesible o no apunta a una imagen válida. En este caso Aspose.Words exporta un ícono con una cruz roja. Esta propiedad devuelve **true** si la imagen original está disponible; devuelve **false** si la imagen original no está disponible y se ofrecerá un ícono de "sin imagen" para guardar.

Al guardar un grupo de formas o una forma que no requiere ninguna imagen, esta propiedad siempre es **true**.

## Ver también

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
