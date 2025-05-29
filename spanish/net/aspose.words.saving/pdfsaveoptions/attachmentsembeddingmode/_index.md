---
title: PdfSaveOptions.AttachmentsEmbeddingMode
linktitle: AttachmentsEmbeddingMode
articleTitle: AttachmentsEmbeddingMode
second_title: Aspose.Words para .NET
description: Personaliza la incrustación de archivos adjuntos en PDF con PdfSaveOptions. Garantiza una integración fluida y optimiza el uso compartido de documentos.
type: docs
weight: 30
url: /es/net/aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/
---
## PdfSaveOptions.AttachmentsEmbeddingMode property

Obtiene o establece un valor que determina cómo se incrustan los archivos adjuntos en el documento PDF.

```csharp
public PdfAttachmentsEmbeddingMode AttachmentsEmbeddingMode { get; set; }
```

## Observaciones

El valor predeterminado esNone y los archivos adjuntos no están incrustados.

Los estándares PDF/A-1, PDF/A-2 y PDF/A-4 normal (no PDF/A-4f) no permiten archivos incrustados. None El valor se utilizará automáticamente.

## Ejemplos

Muestra cómo agregar archivos adjuntos incrustados al documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.AttachmentsEmbeddingMode = PdfAttachmentsEmbeddingMode.Annotations;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", saveOptions);
```

### Ver también

* enum [PdfAttachmentsEmbeddingMode](../../pdfattachmentsembeddingmode/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
