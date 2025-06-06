---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words para .NET
description: Descubra la propiedad PdfSaveOptions ExportParagraphGraphicsToArtifact para controlar los gráficos de párrafo como artefactos, mejorando la claridad visual de su documento.
type: docs
weight: 160
url: /es/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Obtiene o establece un valor que determina si un gráfico de párrafo debe marcarse como artefacto.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` y los gráficos de párrafo (subrayados, énfasis de texto, etc.) se marcarán como "Span" en la estructura lógica del documento.

Cuando el valor es`verdadero` Los gráficos del párrafo se marcarán como "Artefacto".

Este valor se ignora cuando[`ExportDocumentStructure`](../exportdocumentstructure/) es`FALSO` .

## Ejemplos

Muestra cómo exportar gráficos de párrafo como artefactos (subrayados, énfasis de texto, etc.).

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
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
