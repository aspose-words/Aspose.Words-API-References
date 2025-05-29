---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImagesFolderAlias i MarkdownSaveOptions för att enkelt hantera bild-URI:er i dina dokument. Effektivisera ditt arbetsflöde med denna viktiga funktion!
type: docs
weight: 90
url: /sv/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Anger namnet på mappen som används för att konstruera bild-URI:er som skrivs in i ett dokument. Standardvärdet är en tom sträng.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) iMarkdown format, Aspose.Words behöver spara alla bilder som är inbäddade i dokumentet som fristående filer. [`ImagesFolder`](../imagesfolder/) låter dig ange var bilderna ska sparas and `ImagesFolderAlias` låter dig ange hur bildens URI:er ska konstrueras.

Om`ImagesFolderAlias` inte är en tom sträng, så kommer bild-URI:n som skrivits till Markdown att varaImagesFolderAlias + &lt;bildfilnamn&gt;.

Om`ImagesFolderAlias` är en tom sträng, så kommer bild-URI:n written till Markdown att varaImagesFolder + &lt;bildfilnamn&gt;.

Om`ImagesFolderAlias` är satt till '.' (punkt), så kommer bildfilen name att skrivas till Markdown utan sökväg oavsett andra alternativ.

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
