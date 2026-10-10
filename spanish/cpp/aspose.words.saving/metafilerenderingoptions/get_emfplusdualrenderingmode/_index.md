---
title: "Método Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode"
linktitle: "get_EmfPlusDualRenderingMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode. Obtiene o establece un valor que determina cómo se deben renderizar los metarchivos EMF+ Dual en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/metafilerenderingoptions/get_emfplusdualrenderingmode/
---
## MetafileRenderingOptions::get_EmfPlusDualRenderingMode method


Obtiene o establece un valor que determina cómo se deben renderizar los metarchivos EMF+ Dual.

```cpp
Aspose::Words::Saving::EmfPlusDualRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode() const
```

## Observaciones


Los metarchivos EMF+ Dual contienen tanto partes EMF+ como EMF. MS Word y GDI+ siempre renderizan la parte EMF+. Actualmente Aspose.Words no soporta completamente todos los registros EMF+ y, en algunos casos, el resultado de renderizado de la parte EMF se ve mejor que el de la parte EMF+.

Esta opción se usa solo cuando el metarchivo se renderiza como gráficos vectoriales. Cuando el metarchivo se renderiza a bitmap, siempre se usa la parte EMF+.

El valor predeterminado es [EmfPlusWithFallback](../../emfplusdualrenderingmode/).
## Ver también

* Enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
