---
title: PdfSaveOptions.AttachmentsEmbeddingMode
linktitle: AttachmentsEmbeddingMode
articleTitle: AttachmentsEmbeddingMode
second_title: Aspose.Words för .NET
description: Anpassa hur bilagor bäddas in i PDF-filer med PdfSaveOptions. Säkerställ sömlös integration och optimerad dokumentdelning.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/
---
## PdfSaveOptions.AttachmentsEmbeddingMode property

Hämtar eller anger ett värde som avgör hur bilagor bäddas in i PDF-dokumentet.

```csharp
public PdfAttachmentsEmbeddingMode AttachmentsEmbeddingMode { get; set; }
```

## Anmärkningar

Standardvärdet ärNone och bilagor är inte inbäddade.

PDF/A-1, PDF/A-2 och vanliga PDF/A-4 (inte PDF/A-4f) standarder tillåter inte inbäddade filer. None värdet kommer att användas automatiskt.

## Exempel

Visar hur man lägger till inbäddade bilagor i PDF-dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.AttachmentsEmbeddingMode = PdfAttachmentsEmbeddingMode.Annotations;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", saveOptions);
```

### Se även

* enum [PdfAttachmentsEmbeddingMode](../../pdfattachmentsembeddingmode/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
