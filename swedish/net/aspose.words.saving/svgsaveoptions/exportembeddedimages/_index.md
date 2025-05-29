---
title: SvgSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen SvgSaveOptions ExportEmbeddedImages låter dig bädda in bilder i SVG-filer som base64, vilket förbättrar portabiliteten och hanterar filstorleken.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

Anger om bilder ska bäddas in i SVG-dokumentet som base64. Tänk på att aktivering av det här alternativet kan leda till en betydande ökning av storleken på den utgående SVG-filen.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

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
