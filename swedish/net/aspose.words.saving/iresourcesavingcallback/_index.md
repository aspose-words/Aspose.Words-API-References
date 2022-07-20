---
title: IResourceSavingCallback
second_title: Aspose.Words för .NET API Referens
description: Implementera det här gränssnittet om du vill styra hur Aspose.Words sparar externa resurser bilder teckensnitt och css när du sparar ett dokument till HTML eller SVG med fast sida.
type: docs
weight: 4930
url: /sv/net/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface

Implementera det här gränssnittet om du vill styra hur Aspose.Words sparar externa resurser (bilder, teckensnitt och css) när du sparar ett dokument till HTML eller SVG med fast sida.

```csharp
public interface IResourceSavingCallback
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ResourceSaving](../../aspose.words.saving/iresourcesavingcallback/resourcesaving)(ResourceSavingArgs) | Anropas när Aspose.Words sparar en extern resurs till fasta HTML- eller SVG-format på sidan. |

### Exempel

Visar hur man använder en återuppringning för att spåra externa resurser som skapas när ett dokument konverteras till HTML.

```csharp
public void ResourceSavingCallback()
{
    Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

    FontSavingCallback callback = new FontSavingCallback();

    HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
    {
        ResourceSavingCallback = callback
    };

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    Console.WriteLine(callback.GetText());
}

private class FontSavingCallback : IResourceSavingCallback
{
    /// <summary>
    /// Anropas när Aspose.Words sparar en extern resurs till fixerad HTML eller SVG.
    /// </summary>
    public void ResourceSaving(ResourceSavingArgs args)
    {
        mText.AppendLine($"Original document URI:\t{args.Document.OriginalFileName}");
        mText.AppendLine($"Resource being saved:\t{args.ResourceFileName}");
        mText.AppendLine($"Full uri after saving:\t{args.ResourceFileUri}\n");
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private readonly StringBuilder mText = new StringBuilder();
}
```

Visar hur man använder en återuppringning för att skriva ut URI:erna för externa resurser som skapats när ett dokument konverterades till HTML.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // En mapp specificerad av ResourcesFolderAlias kommer att innehålla resurserna istället för ResourcesFolder.
    // Vi måste se till att mappen finns innan strömmarna kan lägga sina resurser i den.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Räknar och skriver ut URI:er för resurser som finns i när de konverteras till fast HTML.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Om vi ställer in ett mappalias i SaveOptions-objektet kommer vi att kunna skriva ut det härifrån.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Som standard använder 'ResourceFileUri' systemmappen för teckensnitt.
                // För att undvika problem på andra plattformar måste du uttryckligen ange sökvägen för typsnitten.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Om vi har angett en mapp i egenskapen "ResourcesFolderAlias",
        // vi kommer också att behöva omdirigera varje ström för att placera dess resurs i den mappen.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
