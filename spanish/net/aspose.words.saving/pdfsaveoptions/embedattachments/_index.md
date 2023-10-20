---
title: PdfSaveOptions.EmbedAttachments
linktitle: EmbedAttachments
articleTitle: EmbedAttachments
second_title: Aspose.Words para .NET
description: PdfSaveOptions EmbedAttachments propiedad. Obtiene o establece un valor que determina si se incrustan o no archivos adjuntos en el documento PDF en C#.
type: docs
weight: 110
url: /es/net/aspose.words.saving/pdfsaveoptions/embedattachments/
---
## PdfSaveOptions.EmbedAttachments property

Obtiene o establece un valor que determina si se incrustan o no archivos adjuntos en el documento PDF.

```csharp
public bool EmbedAttachments { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` los archivos adjuntos no están incrustados.

Cuando el valor es`verdadero` Los archivos adjuntos están incrustados en el documento PDF.

No se admite la incrustación de archivos adjuntos al guardar en formato PDF/A y PDF/UA. `FALSO` El valor se utilizará automáticamente.

No se admite la incrustación de archivos adjuntos cuando el cifrado está habilitado.`FALSO` value se utilizará automáticamente.

## Ejemplos

Muestra cómo agregar archivos adjuntos incrustados al documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions options = new PdfSaveOptions();
options.EmbedAttachments = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
