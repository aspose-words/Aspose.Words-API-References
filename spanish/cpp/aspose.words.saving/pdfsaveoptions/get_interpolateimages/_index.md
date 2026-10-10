---
title: "Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages método"
linktitle: "get_InterpolateImages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages método. Un indicador que indica si la interpolación de imágenes debe ser realizada por un lector compatible. Cuando se especifica **false**, el indicador no se escribe en el documento de salida y se utiliza el comportamiento predeterminado del lector en su lugar en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_interpolateimages/
---
## PdfSaveOptions::get_InterpolateImages method


Una bandera que indica si la interpolación de imágenes debe ser realizada por un lector compatible. Cuando se especifica **false**, la bandera no se escribe en el documento de salida y se utiliza el comportamiento predeterminado del lector.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages() const
```

## Observaciones


Cuando la resolución de una imagen de origen es significativamente menor que la del dispositivo de salida, cada muestra de origen cubre muchos píxeles del dispositivo. Como resultado, las imágenes pueden aparecer dentadas o pixeladas. Estos artefactos visuales pueden reducirse aplicando un algoritmo de interpolación de imágenes durante el renderizado. En lugar de pintar todos los píxeles cubiertos por una muestra de origen con el mismo color, la interpolación de imágenes intenta producir una transición suave entre los valores de muestra adyacentes.

Un lector compatible puede optar por no implementar esta característica del PDF, o puede utilizar cualquier implementación específica de interpolación que desee.

El valor predeterminado es **false**.

El indicador de interpolación está prohibido por la conformidad PDF/A. Se utilizará automáticamente el valor **false** al guardar en PDF/A.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
