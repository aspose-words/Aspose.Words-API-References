---
title: MarkdownSaveOptions.ImagesFolder
second_title: Aspose.Words för .NET API Referens
description: MarkdownSaveOptions fast egendom. Anger den fysiska mappen där bilderna sparas när ett dokument exporteras till Markdown formatera. Standard är en tom sträng.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Anger den fysiska mappen där bilderna sparas när ett dokument exporteras till Markdown formatera. Standard är en tom sträng.

```csharp
public string ImagesFolder { get; set; }
```

### Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) iMarkdownformat, Aspose.Words måste spara alla bilder som är inbäddade i dokumentet som fristående filer. `ImagesFolder` låter dig ange var bilderna ska sparas.

Om du sparar ett dokument i en fil och anger ett filnamn, sparar Aspose.Words, som standard, bilderna i samma mapp där dokumentfilen sparas. Använda sig av`ImagesFolder` för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström, har Aspose.Words ingen folder där bilderna ska sparas, men måste fortfarande spara bilderna någonstans. I det här fallet, måste du ange en tillgänglig mapp i`ImagesFolder` egenskap.

Om mappen som anges av`ImagesFolder` inte finns skapas den automatiskt.

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


