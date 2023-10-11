---
title: MarkdownSaveOptions.ImagesFolderAlias
second_title: Aspose.Words för .NET API Referens
description: MarkdownSaveOptions fast egendom. Anger namnet på mappen som används för att konstruera bildURIer inskrivna i ett dokument. Standard är en tom sträng.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Anger namnet på mappen som används för att konstruera bild-URI:er inskrivna i ett dokument. Standard är en tom sträng.

```csharp
public string ImagesFolderAlias { get; set; }
```

### Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) iMarkdown format, Aspose.Words måste spara alla bilder som är inbäddade i dokumentet som fristående filer. [`ImagesFolder`](../imagesfolder/) låter dig ange var bilderna ska sparas och `ImagesFolderAlias` gör det möjligt att specificera hur bildens URI:er kommer att konstrueras.

Om`ImagesFolderAlias` inte är en tom sträng, så blir bilden URI written till MarkdownImagesFolderAlias + &lt;bildfilnamn&gt;.

Om`ImagesFolderAlias` är en tom sträng, då blir bilden URI written till MarkdownImagesFolder + &lt;bildfilnamn&gt;.

Om`ImagesFolderAlias`är satt till '.' (prick), då kommer bildfilen name att skrivas till Markdown utan sökväg oavsett andra alternativ.

### Exempel

Visar hur man anger namnet på mappen som används för att konstruera bild-URI:er.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
Image image = Image.FromFile(ImageDir + "Logo.jpg");
builder.InsertImage(image);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Använd egenskapen "ImagesFolder" för att tilldela en mapp i det lokala filsystemet som
// Aspose.Words kommer att spara alla dokumentets länkade bilder.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Använd egenskapen "ImagesFolderAlias" för att använda den här mappen
// när du konstruerar bild-URI:er istället för bildmappens namn.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

Visar hur man anger namnet på mappen som används för att konstruera bild-URI:er (.NetStandard 2.0).

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(bitmap);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Använd egenskapen "ImagesFolder" för att tilldela en mapp i det lokala filsystemet som
// Aspose.Words kommer att spara alla dokumentets länkade bilder.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Använd egenskapen "ImagesFolderAlias" för att använda den här mappen
// när du konstruerar bild-URI:er istället för bildmappens namn.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Se även

* class [MarkdownSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../markdownsaveoptions/)
* hopsättning [Aspose.Words](../../../)


