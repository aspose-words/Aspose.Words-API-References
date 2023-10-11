---
title: PdfSaveOptions.EmbedAttachments
second_title: Aspose.Words för .NET API Referens
description: PdfSaveOptions fast egendom. Hämtar eller ställer in ett värde som avgör om bilagor ska bäddas in i PDFdokumentet eller inte.
type: docs
weight: 110
url: /sv/net/aspose.words.saving/pdfsaveoptions/embedattachments/
---
## PdfSaveOptions.EmbedAttachments property

Hämtar eller ställer in ett värde som avgör om bilagor ska bäddas in i PDF-dokumentet eller inte.

```csharp
public bool EmbedAttachments { get; set; }
```

### Anmärkningar

Standardvärdet är`falsk`och bilagor är inte inbäddade.

När värdet är`Sann` bilagor är inbäddade i PDF-dokumentet.

Inbäddning av bilagor stöds inte när du sparar till PDF/A och PDF/UA-kompatibilitet. `falsk` värdet kommer att användas automatiskt.

Inbäddning av bilagor stöds inte när kryptering är aktiverad.`falsk` value kommer att användas automatiskt.

### Exempel

Visar hur man lägger till inbäddade bilagor till PDF-dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions options = new PdfSaveOptions();
options.EmbedAttachments = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../pdfsaveoptions/)
* hopsättning [Aspose.Words](../../../)


