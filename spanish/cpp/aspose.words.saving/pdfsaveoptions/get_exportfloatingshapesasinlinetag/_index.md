---
title: "Método Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag"
linktitle: "get_ExportFloatingShapesAsInlineTag"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag. Obtiene o establece un valor que determina si las formas flotantes se exportan como etiquetas en línea en la estructura del documento en C++."
type: docs
weight: 16500
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_exportfloatingshapesasinlinetag/
---
## PdfSaveOptions::get_ExportFloatingShapesAsInlineTag method


Obtiene o establece un valor que determina si las formas flotantes se exportan como etiquetas en línea en la estructura del documento.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag() const
```

## Observaciones


El valor predeterminado es **false** y las formas flotantes se exportarán como etiquetas de nivel de bloque, colocadas después del párrafo al que están ancladas.

Cuando el valor es **true**, las formas flotantes se exportarán como etiquetas en línea, ubicadas dentro del párrafo donde están ancladas.

Este valor se ignora cuando [ExportDocumentStructure](../get_exportdocumentstructure/) es **false**.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
