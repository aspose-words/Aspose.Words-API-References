---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact método"
linktitle: "get_ExportParagraphGraphicsToArtifact"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact método. Obtiene o establece un valor que determina si un gráfico de párrafo debe marcarse como un artefacto en C++."
type: docs
weight: 17500
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_exportparagraphgraphicstoartifact/
---
## PdfSaveOptions::get_ExportParagraphGraphicsToArtifact method


Obtiene o establece un valor que determina si un gráfico de párrafo debe marcarse como un artefacto.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact() const
```

## Observaciones


El valor predeterminado es **false** y los gráficos de párrafo (subrayados, énfasis de texto, etc.) se marcarán como "Span" en la estructura lógica del documento.

Cuando el valor es **true** los gráficos de párrafo se marcarán como "Artifact".

Este valor se ignora cuando [ExportDocumentStructure](../get_exportdocumentstructure/) es **false**.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
