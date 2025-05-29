---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlSaveOptions DocumentSplitCriteria för att optimera dokumentsparning i HTML-, EPUB- och AZW3-format. Förbättra din formateringskontroll idag!
type: docs
weight: 80
url: /sv/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Anger hur dokumentet ska delas upp när det sparas tillHtml , Epub ellerAzw3 format. Standard ärNone för HTML och HeadingParagraph för EPUB och AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## Anmärkningar

Normalt sett vill du att ett dokument ska sparas i HTML-format som en enda fil. Men i vissa fall är det att föredra att dela upp utdata i flera mindre HTML-sidor. När du sparar i HTML-format kommer dessa sidor att matas ut till enskilda filer eller strömmar. När du sparar i EPUB-format kommer de att integreras i motsvarande paket.

Ett dokument kan inte delas när det sparas i MHTML-format.

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
