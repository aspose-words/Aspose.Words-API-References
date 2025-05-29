---
title: HtmlSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words för .NET
description: Upptäck HtmlSaveOptions-kodning för sömlös export av HTML, MHTML och EPUB. Anpassa enkelt kodningen med UTF-8 för optimal kompatibilitet och prestanda.
type: docs
weight: 100
url: /sv/net/aspose.words.saving/htmlsaveoptions/encoding/
---
## HtmlSaveOptions.Encoding property

Anger vilken kodning som ska användas vid export till HTML, MHTML eller EPUB. Standardvärdet är`ny UTF8-kodning(falsk)` (UTF-8 utan BOM).

```csharp
public Encoding Encoding { get; set; }
```

## Exempel

Visar hur man använder en specifik kodning när man sparar ett dokument till .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Använd ett SaveOptions-objekt för att ange kodningen för ett dokument som vi ska spara.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Som standard kommer ett .epub-dokument att ha allt innehåll i en HTML-del.
// Ett delningskriterium låter oss segmentera dokumentet i flera HTML-delar.
// Vi kommer att ställa in kriterierna för att dela upp dokumentet i rubrikstycken.
// Detta är användbart för läsare som inte kan läsa HTML-filer som är större än en viss storlek.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Ange att vi vill exportera dokumentegenskaper.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
