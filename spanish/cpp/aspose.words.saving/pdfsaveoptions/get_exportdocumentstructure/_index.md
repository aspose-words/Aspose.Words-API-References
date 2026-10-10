---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure método"
linktitle: "get_ExportDocumentStructure"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure método. Obtiene o establece un valor que determina si se exporta o no la estructura del documento en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_exportdocumentstructure/
---
## PdfSaveOptions::get_ExportDocumentStructure method


Obtiene o establece un valor que determina si se exporta o no la estructura del documento.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure() const
```

## Observaciones


Este valor se ignora al guardar en PDF/A-1a, PDF/A-2a y PDF/UA-1 porque la estructura del documento es requerida para esta conformidad.

Tenga en cuenta que exportar la estructura del documento incrementa significativamente el consumo de memoria, especialmente en documentos grandes.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
