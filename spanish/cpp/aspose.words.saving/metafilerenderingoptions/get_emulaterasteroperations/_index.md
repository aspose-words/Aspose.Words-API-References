---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations método"
linktitle: "get_EmulateRasterOperations"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations método. Obtiene o establece un valor que determina si las operaciones de trama deben emularse en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterasteroperations/
---
## MetafileRenderingOptions::get_EmulateRasterOperations method


Obtiene o establece un valor que determina si se deben emular o no las operaciones raster.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations() const
```

## Observaciones


Operaciones de trama específicas podrían usarse en metaficheros. No pueden renderizarse directamente a gráficos vectoriales. Emular operaciones de trama requiere una rasterización parcial de los gráficos vectoriales resultantes, lo que puede afectar el rendimiento del renderizado del metafichero.

Cuando este valor se establece en **true**, Aspose.Words emula las operaciones de trama. La salida resultante puede estar parcialmente rasterizada y el rendimiento podría ser más lento.

Cuando este valor se establece en **false**, Aspose.Words no emula las operaciones de trama. Cuando [Aspose.Words](../../../aspose.words/) encuentra una operación de trama en un metafichero, recurre a renderizar el metafichero en un mapa de bits utilizando el sistema operativo.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales.

El valor predeterminado es **true**.
## Ver también

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
