---
title: MarkdownSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen MarkdownSaveOptions ImagesFolder förbättrar dina dokumentexporter genom att ange den ideala mappen för att spara bilder i Markdown-format.
type: docs
weight: 80
url: /sv/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Anger den fysiska mappen där bilder sparas när ett dokument exporteras till Markdown format. Standard är en tom sträng.

```csharp
public string ImagesFolder { get; set; }
```

## Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) iMarkdownformat, Aspose.Words behöver spara alla bilder som är inbäddade i dokumentet som fristående filer. `ImagesFolder` låter dig ange var bilderna ska sparas.

Om du sparar ett dokument i en fil och anger ett filnamn, sparar Aspose.Words som standard bilderna i samma mapp där dokumentfilen är sparad. Använd`ImagesFolder` för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström har Aspose.Words ingen mapp där bilderna ska sparas, men behöver fortfarande spara bilderna någonstans. I det här fallet måste du ange en tillgänglig mapp i`ImagesFolder` egendom.

Om mappen som anges av`ImagesFolder` inte finns, kommer den att skapas automatiskt.

## Exempel

Visar hur man anger namnet på den mapp som används för att konstruera bild-URI:er.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
builder.InsertImage(ImageDir + "Logo.jpg");

string imagesFolder = Path.Combine(ArtifactsDir, "ImagesDir");
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Använd egenskapen "ImagesFolder" för att tilldela en mapp i det lokala filsystemet till vilken
// Aspose.Words sparar alla länkade bilder i dokumentet.
saveOptions.ImagesFolder = imagesFolder;
// Använd egenskapen "ImagesFolderAlias" för att använda den här mappen
// när man konstruerar bild-URI:er istället för bildmappens namn.
saveOptions.ImagesFolderAlias = "http://example.com/bilder";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Se även

* class [MarkdownSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
