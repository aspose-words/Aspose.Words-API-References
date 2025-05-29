---
title: SvgSaveOptions.ResourcesFolderAlias
linktitle: ResourcesFolderAlias
articleTitle: ResourcesFolderAlias
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SvgSaveOptions ResourcesFolderAlias för att anpassa bild-URI:er i SVG-dokument. Förbättra din SVG-utdata med flexibel mappnamngivning!
type: docs
weight: 90
url: /sv/net/aspose.words.saving/svgsaveoptions/resourcesfolderalias/
---
## SvgSaveOptions.ResourcesFolderAlias property

Anger namnet på mappen som används för att konstruera bild-URI:er som skrivs in i ett SVG-dokument. Standard är`null` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

## Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) I SVG-format behöver Aspose.Words spara alla bilder som är inbäddade i dokumentet som fristående filer.[`ResourcesFolder`](../resourcesfolder/) låter dig ange var bilderna ska sparas och`ResourcesFolderAlias` låter dig ange hur bildens URI:er ska konstrueras.

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
