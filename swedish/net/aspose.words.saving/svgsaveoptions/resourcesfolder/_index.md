---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words för .NET
description: SvgSaveOptions ResourcesFolder fast egendom. Anger den fysiska mappen där resurser bilder sparas vid export av ett dokument till Svgformat. Standard ärnull  i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Anger den fysiska mappen där resurser (bilder) sparas vid export av ett dokument till Svg-format. Standard är`null` .

```csharp
public string ResourcesFolder { get; set; }
```

## Anmärkningar

Har effekt endast om[`ExportEmbeddedImages`](../exportembeddedimages/) egendom är`falsk`.

När du sparar en[`Document`](../../../aspose.words/document/) i SVG-format måste Aspose.Words spara all bilder som är inbäddade i dokumentet som fristående filer.`ResourcesFolder` låter dig ange var bilderna ska sparas och[`ResourcesFolderAlias`](../resourcesfolderalias/) tillåter att specificera hur bildens URI:er kommer att konstrueras.

Om du sparar ett dokument i en fil och anger ett filnamn, sparar Aspose.Words, som standard, bilderna i samma mapp där dokumentfilen sparas. Använda sig av`ResourcesFolder` för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström, har Aspose.Words ingen mapp där du kan spara bilderna, men behöver fortfarande spara bilderna någonstans. I det här fallet måste du ange en tillgänglig mapp i`ResourcesFolder` fast egendom

## Exempel

Visar hur man manipulerar och skriver ut URI:erna för länkade resurser som skapas när ett dokument konverteras till .svg.

```csharp
public void SvgResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    SvgSaveOptions options = new SvgSaveOptions
    {
        SaveFormat = SaveFormat.Svg,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "SvgResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "SvgResourceFolderAlias",
        ShowPageBorder = false,

        ResourceSavingCallback = new ResourceUriPrinter()
    };

    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
}

/// <summary>
/// Räknar och skriver ut URI:er för resurser som finns i när de konverteras till .svg.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Console.WriteLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");
        Console.WriteLine("\t" + args.ResourceFileUri);
    }

    private int mSavedResourceCount;
}
```

### Se även

* class [SvgSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
