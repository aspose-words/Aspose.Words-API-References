---
title: HtmlSaveOptions.DocumentSplitCriteria
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger hur dokumentet ska delas när du sparar tillHtml ellerEpub formatera. Standard ärNone för HTML och HeadingParagraph för EPUB.
type: docs
weight: 80
url: /sv/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Anger hur dokumentet ska delas när du sparar tillHtml ellerEpub formatera. Standard ärNone för HTML och HeadingParagraph för EPUB.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

### Anmärkningar

Normalt vill du ha ett dokument sparat i HTML som en enda fil. Men i vissa fall är det att föredra att dela upp resultatet i flera mindre HTML-sidor. När du sparar i HTML-format kommer dessa sidor att matas ut till enskilda filer eller strömmar. När du sparar till EPUB-format kommer de att inkorporeras i motsvarande paket.

Ett dokument kan inte delas när du sparar i MHTML-format.

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


