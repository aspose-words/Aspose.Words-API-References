---
title: ResourceSavingArgs.ResourceFileUri
linktitle: ResourceFileUri
articleTitle: ResourceFileUri
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ResourceSavingArgs ResourceFileUri för att enkelt hantera och referera till resursfiler i dina dokument. Öka effektiviteten idag!
type: docs
weight: 40
url: /sv/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

Hämtar eller ställer in den enhetliga resursidentifierare (URI) som används för att referera till resursfilen från dokumentet.

```csharp
public string ResourceFileUri { get; set; }
```

## Anmärkningar

Den här egenskapen låter dig ändra URI:er för resursfiler som exporteras till HTML- eller SVG-dokument med fast sida.

Aspose.Words genererar automatiskt en URI för varje resursfil vid export till fast sidformat i HTML eller SVG. De genererade URI:erna refererar till resursfiler som sparats av Aspose.Words. URI:erna kan dock vara felaktiga om resursfiler ska flyttas till en annan plats eller om resursfiler sparas i strömmar. Den här egenskapen gör det möjligt att korrigera URI:er i dessa fall.

När händelsen utlöses innehåller den här egenskapen den URI som genererades av Aspose.Words. Du kan ändra värdet för den här egenskapen för att tillhandahålla en anpassad URI för resursfilen.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

## Exempel

Visar hur man använder en återanropsfunktion för att spåra externa resurser som skapats vid konvertering av ett dokument till HTML.

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
    /// Anropas när Aspose.Words sparar en extern resurs till en fast sida i HTML eller SVG.
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

### Se även

* class [ResourceSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
