---
title: "Método Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf"
linktitle: "get_UseEmfEmbeddedToWmf"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf. Obtiene o establece un valor que determina cómo se deben renderizar los metarchivos WMF con metarchivos EMF incrustados en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.saving/metafilerenderingoptions/get_useemfembeddedtowmf/
---
## MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method


Obtiene o establece un valor que determina cómo se deben renderizar los metarchivos WMF con metarchivos EMF incrustados.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf() const
```

## Observaciones


Los archivos WMF podrían contener datos EMF incrustados. MS Word, en la mayoría de los casos, utiliza datos EMF incrustados. GDI+ siempre utiliza datos WMF.

Cuando este valor se establece en **true**, Aspose.Words utiliza datos EMF incrustados al renderizar.

Cuando este valor se establece en **false**, Aspose.Words utiliza datos WMF al renderizar.

Esta opción se usa solo cuando el metafichero se renderiza como gráficos vectoriales. Cuando el metafichero se renderiza a mapa de bits, siempre se utilizan datos WMF.

El valor predeterminado es **true**.
## Ver también

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
