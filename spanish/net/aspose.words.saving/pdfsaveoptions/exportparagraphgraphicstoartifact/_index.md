---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Obtiene o establece un valor que determina si un gráfico de párrafo debe marcarse como un artefacto.
type: docs
weight: 160
url: /es/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Obtiene o establece un valor que determina si un gráfico de párrafo debe marcarse como un artefacto.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

### Observaciones

El valor predeterminado es`FALSO` y los gráficos de párrafo (subrayados, énfasis de texto, etc.) se marcarán como "Span" en la estructura lógica del documento.

Cuando el valor es`verdadero` los gráficos del párrafo se marcarán como "Artefacto".

Este valor se ignora cuando[`ExportDocumentStructure`](../exportdocumentstructure/) es`FALSO` .

### Ejemplos

Muestra cómo exportar gráficos de párrafos como artefactos (subrayados, énfasis de texto, etc.).

```csharp
Document doc = new Document(MyDir + "PDF artifacts.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.ExportDocumentStructure = true;
saveOptions.ExportParagraphGraphicsToArtifact = true;
saveOptions.TextCompression = PdfTextCompression.None;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportParagraphGraphicsToArtifact.pdf", saveOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


