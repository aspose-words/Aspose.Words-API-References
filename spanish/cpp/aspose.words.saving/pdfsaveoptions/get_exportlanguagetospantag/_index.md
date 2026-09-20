---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag método"
linktitle: "get_ExportLanguageToSpanTag"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag método. Obtiene o establece un valor que determina si crear o no una etiqueta \"Span\" en la estructura del documento para exportar el idioma del texto en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_exportlanguagetospantag/
---
## PdfSaveOptions::get_ExportLanguageToSpanTag method


Obtiene o establece un valor que determina si se crea o no una etiqueta "Span" en la estructura del documento para exportar el idioma del texto.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag() const
```

## Observaciones


El valor predeterminado es **false** y el atributo "Lang" se adjunta a una secuencia de contenido marcado en el flujo de contenido de una página.

Cuando el valor es **true** se crea una etiqueta "Span" para el texto con idioma no predeterminado y el atributo "Lang" se adjunta a esta etiqueta.

Este valor se ignora cuando [ExportDocumentStructure](../get_exportdocumentstructure/) es **false**.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
