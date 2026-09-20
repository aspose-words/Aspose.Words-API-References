---
title: "Aspose::Words::Saving::MetafileRenderingMode enum"
linktitle: "MetafileRenderingMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MetafileRenderingMode enum. Especifica cómo Aspose.Words debe renderizar los metaficheros WMF y EMF en C++."
type: docs
weight: 69000
url: /es/cpp/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enum


Especifica cómo Aspose.Words debe renderizar los metarchivos WMF y EMF.

```cpp
enum class MetafileRenderingMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| VectorWithFallback | 0 | Aspose.Words intenta renderizar un metafichero como gráficos vectoriales. Si Aspose.Words no puede renderizar correctamente algunos de los registros del metafichero como gráficos vectoriales, entonces Aspose.Words renderiza este metafichero a un mapa de bits. |
| Vector | 1 | Aspose.Words renderiza un metafichero como gráficos vectoriales. |
| Bitmap | 2 | Aspose.Words invoca GDI+ para renderizar un metafichero a un bitmap y luego guarda el bitmap en el documento de salida. |

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
