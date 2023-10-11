---
title: HtmlSaveOptions.ImagesFolder
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger den fysiska mappen där bilder sparas vid export av ett dokument till HTMLformat. Standard är en tom sträng.
type: docs
weight: 360
url: /sv/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Anger den fysiska mappen där bilder sparas vid export av ett dokument till HTML-format. Standard är en tom sträng.

```csharp
public string ImagesFolder { get; set; }
```

### Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) i HTML-format måste Aspose.Words spara alla -bilder som är inbäddade i dokumentet som fristående filer.`ImagesFolder` låter dig ange var bilderna ska sparas och[`ImagesFolderAlias`](../imagesfolderalias/) tillåter att specificera hur bildens URI:er kommer att konstrueras.

Om du sparar ett dokument i en fil och anger ett filnamn, sparar Aspose.Words, som standard, -bilderna i samma mapp där dokumentfilen sparas. Använda sig av`ImagesFolder` för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström så har Aspose.Words ingen mapp där bilderna ska sparas, men behöver ändå spara bilderna någonstans. I det här fallet måste du ange en tillgänglig mapp i`ImagesFolder` egendom eller tillhandahålla anpassade strömmar via the[`ImageSavingCallback`](../imagesavingcallback/) händelsehanterare.

Om mappen som anges av`ImagesFolder` inte finns skapas den automatiskt.

[`ResourceFolder`](../resourcefolder/) är ett annat sätt att ange en mapp där bilderna ska sparas.

### Exempel

Visar hur man anger mappen för lagring av länkade bilder efter att ha sparats i .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Ställ in ett alternativ för att exportera formulärfält som vanlig text istället för HTML-inmatningselement.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


