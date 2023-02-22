---
title: HtmlFixedSaveOptions.ResourcesFolder
second_title: Aspose.Words för .NET API Referens
description: HtmlFixedSaveOptions fast egendom. Anger den fysiska mappen där resurser bilder teckensnitt css sparas vid export av ett dokument till HTMLformat. Standard ärnull .
type: docs
weight: 140
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/
---
## HtmlFixedSaveOptions.ResourcesFolder property

Anger den fysiska mappen där resurser (bilder, teckensnitt, css) sparas vid export av ett dokument till HTML-format. Standard är`null` .

```csharp
public string ResourcesFolder { get; set; }
```

### Anmärkningar

Har effekt endast om[`ExportEmbeddedImages`](../exportembeddedimages/) egendom är falsk.

När du sparar en[`Document`](../../../aspose.words/document/) i HTML-format måste Aspose.Words spara all bilder inbäddade i dokumentet som fristående filer.`ResourcesFolder` låter dig ange var bilderna ska sparas och[`ResourcesFolderAlias`](../resourcesfolderalias/) tillåter att specificera hur bildens URI:er kommer att konstrueras.

Om du sparar ett dokument i en fil och anger ett filnamn, sparar Aspose.Words, som standard, bilderna i samma mapp där dokumentfilen sparas. Använda sig av`ResourcesFolder` för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström, har Aspose.Words ingen mapp där du kan spara bilderna, men behöver fortfarande spara bilderna någonstans. I det här fallet måste du ange en tillgänglig mapp genom att använda`ResourcesFolder` fast egendom

### Exempel

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

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* hopsättning [Aspose.Words](../../../)


