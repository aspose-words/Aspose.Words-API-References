---
title: HtmlSaveOptions.Encoding
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger kodningen som ska användas vid export till HTML MHTML eller EPUB. Standardvärdet ärny UTF8 Encodingfalse UTF8 utan stycklista.
type: docs
weight: 100
url: /sv/net/aspose.words.saving/htmlsaveoptions/encoding/
---
## HtmlSaveOptions.Encoding property

Anger kodningen som ska användas vid export till HTML, MHTML eller EPUB. Standardvärdet är`ny UTF8 Encoding(false)` (UTF-8 utan stycklista).

```csharp
public Encoding Encoding { get; set; }
```

### Exempel

Visar hur du använder en specifik kodning när du sparar ett dokument i .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Använd ett SaveOptions-objekt för att ange kodningen för ett dokument som vi ska spara.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Som standard kommer ett utdata .epub-dokument att ha allt innehåll i en HTML-del.
// Ett delat kriterium tillåter oss att segmentera dokumentet i flera HTML-delar.
// Vi kommer att ställa in kriterierna för att dela upp dokumentet i rubriker.
// Detta är användbart för läsare som inte kan läsa HTML-filer som är större än en viss storlek.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Ange att vi vill exportera dokumentegenskaper.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


