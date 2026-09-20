---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage método"
linktitle: "get_EmulateRenderingToSizeOnPage"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage método. Obtiene o establece un valor que determina si el renderizado del metafichero emula la visualización del metafichero según el tamaño en la página o la visualización del metafichero en su tamaño predeterminado en C++."
type: docs
weight: 4334
url: /es/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method


Obtiene o establece un valor que determina si el renderizado del metarchivo emula la visualización del metarchivo según el tamaño en la página o la visualización del metarchivo en su tamaño predeterminado.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage() const
```

## Observaciones


Cuando los metaficheros se muestran en MS Word, algunos gráficos pueden escalarse según el tamaño real del metafichero en píxeles. Es decir, incluso el zoom puede afectar la visualización del metafichero.

Cuando este valor se establece en **true**, Aspose.Words emula el renderizado de acuerdo con el tamaño del metafichero en la página. El tamaño en píxeles se calcula a partir del tamaño del metafichero en la página y la [EmulateRenderingToSizeOnPageResolution](../get_emulaterenderingtosizeonpageresolution/) especificada.

Cuando este valor se establece en **false**, Aspose.Words emula el renderizado del metafichero a su tamaño predeterminado en píxeles.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales.

El valor predeterminado es **true**.
## Ver también

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
