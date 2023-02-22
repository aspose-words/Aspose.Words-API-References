---
title: SvgSaveOptions.SaveFormat
second_title: Aspose.Words för .NET API Referens
description: SvgSaveOptions fast egendom. Anger formatet som dokumentet kommer att sparas i om detta sparaalternativobjekt används. Kan endastSvg .
type: docs
weight: 70
url: /sv/net/aspose.words.saving/svgsaveoptions/saveformat/
---
## SvgSaveOptions.SaveFormat property

Anger formatet som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan endastSvg .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Exempel

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SvgSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../svgsaveoptions/)
* hopsättning [Aspose.Words](../../../)


