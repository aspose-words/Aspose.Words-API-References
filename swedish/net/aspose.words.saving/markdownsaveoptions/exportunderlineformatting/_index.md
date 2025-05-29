---
title: MarkdownSaveOptions.ExportUnderlineFormatting
linktitle: ExportUnderlineFormatting
articleTitle: ExportUnderlineFormatting
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen MarkdownSaveOptions ExportUnderlineFormatting förbättrar din textexport. Kontrollera understrykningsformatering enkelt med den här booleska inställningen.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/markdownsaveoptions/exportunderlineformatting/
---
## MarkdownSaveOptions.ExportUnderlineFormatting property

Hämtar eller ställer in ett booleskt värde som anger att antingen understruken textformatering ska exporteras som en sekvens av två plustecken "++". Standardvärdet är`falsk` .

```csharp
public bool ExportUnderlineFormatting { get; set; }
```

## Exempel

Visar hur man exporterar understrykningsformatering som ++.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Single;
builder.Write("Lorem ipsum. Dolor sit amet.");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions() { ExportUnderlineFormatting = true };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

### Se även

* class [MarkdownSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
