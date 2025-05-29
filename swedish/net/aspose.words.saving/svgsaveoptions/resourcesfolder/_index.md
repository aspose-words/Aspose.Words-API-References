---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words för .NET
description: Upptäck hur du ställer in ResourcesFolder i SvgSaveOptions för effektiv bildlagring när du exporterar dokument till SVG-format. Optimera ditt arbetsflöde idag!
type: docs
weight: 80
url: /sv/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Anger den fysiska mappen där resurser (bilder) sparas när ett dokument exporteras till Svg-format. Standard är`null` .

```csharp
public string ResourcesFolder { get; set; }
```

## Anmärkningar

Har endast effekt om[`ExportEmbeddedImages`](../exportembeddedimages/) egendomen är`falsk`.

När du sparar en[`Document`](../../../aspose.words/document/) I SVG-format behöver Aspose.Words spara alla bilder som är inbäddade i dokumentet som fristående filer.`ResourcesFolder` låter dig ange var bilderna ska sparas och[`ResourcesFolderAlias`](../resourcesfolderalias/) låter dig ange hur bildens URI:er ska konstrueras.

Om du sparar ett dokument i en fil och anger ett filnamn, sparar Aspose.Words som standard -bilderna i samma mapp där dokumentfilen är sparad.`ResourcesFolder` för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström har Aspose.Words ingen mapp där bilderna ska sparas, men behöver fortfarande spara bilderna någonstans. I det här fallet måste du ange en tillgänglig mapp i`ResourcesFolder` egendom

## Exempel

Visar hur man manipulerar och skriver ut URI:er för länkade resurser som skapats vid konvertering av ett dokument till .svg.

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
/// Räknar och skriver ut URI:er för resurser som finns i formatet allt eftersom de konverteras till .svg.
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
