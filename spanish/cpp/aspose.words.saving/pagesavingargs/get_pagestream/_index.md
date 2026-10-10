---
title: "Aspose::Words::Saving::PageSavingArgs::get_PageStream method"
linktitle: "get_PageStream"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PageSavingArgs::get_PageStream method. Permite especificar el flujo donde se guardará la página del documento en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.saving/pagesavingargs/get_pagestream/
---
## PageSavingArgs::get_PageStream method


Permite especificar el flujo donde se guardará la página del documento.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::PageSavingArgs::get_PageStream() const
```

## Observaciones


Esta propiedad le permite guardar páginas de documentos en flujos en lugar de archivos.

El valor predeterminado es **null**. Cuando esta propiedad es **null**, la página del documento se guardará en un archivo especificado en la propiedad [PageFileName](../get_pagefilename/).

Si tanto [PageStream](./) como [PageFileName](../get_pagefilename/) están configurados, se utilizará PageStream.

## Ver también

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
