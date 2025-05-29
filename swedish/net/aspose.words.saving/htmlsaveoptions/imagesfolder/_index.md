---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlSaveOptions ImagesFolder. Ställ enkelt in mappen för att spara bilder när du exporterar dokument till HTML. Effektivisera ditt arbetsflöde idag!
type: docs
weight: 360
url: /sv/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Anger den fysiska mappen där bilder sparas när ett dokument exporteras till HTML-format. Standardvärdet är en tom sträng.

```csharp
public string ImagesFolder { get; set; }
```

## Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) I HTML-format behöver Aspose.Words spara alla bilder som är inbäddade i dokumentet som fristående filer.`ImagesFolder` låter dig ange var bilderna ska sparas och[`ImagesFolderAlias`](../imagesfolderalias/) låter dig ange hur bildens URI:er ska konstrueras.

Om du sparar ett dokument i en fil och anger ett filnamn, sparar Aspose.Words som standard -bilderna i samma mapp där dokumentfilen är sparad.`ImagesFolder` för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström har Aspose.Words ingen mapp där bilderna ska sparas, men behöver fortfarande spara bilderna någonstans. I det här fallet måste du ange en tillgänglig mapp i`ImagesFolder` egendom eller tillhandahålla anpassade strömmar via the[`ImageSavingCallback`](../imagesavingcallback/) händelsehanterare.

Om mappen som anges av`ImagesFolder` inte finns, kommer den att skapas automatiskt.

[`ResourceFolder`](../resourcefolder/) är ett annat sätt att ange en mapp där bilder ska sparas.

## Exempel

Visar hur man anger mappen för att lagra länkade bilder efter att de har sparats till .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Ange ett alternativ för att exportera formulärfält som vanlig text istället för HTML-inmatningselement.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
