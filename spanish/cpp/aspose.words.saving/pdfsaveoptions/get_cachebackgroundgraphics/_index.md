---
title: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics method"
linktitle: "get_CacheBackgroundGraphics"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics method. Obtiene o establece un valor que determina si se deben almacenar en caché los gráficos colocados en el fondo del documento en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_cachebackgroundgraphics/
---
## PdfSaveOptions::get_CacheBackgroundGraphics method


Obtiene o establece un valor que determina si se almacenan en caché o no los gráficos colocados en el fondo del documento.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics() const
```

## Observaciones


El valor predeterminado es **true** y los gráficos de fondo se escriben en el documento PDF como un xObject.

Cuando el valor es **false**, los gráficos de fondo no se almacenan en caché.

Algunas formas no son compatibles con el almacenamiento en caché (formas con campos, marcadores, HRefs).

[Document](../../../aspose.words/document/) background graphic is various shapes, charts, images placed in the footer or header, well as background and border of a page. 
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
