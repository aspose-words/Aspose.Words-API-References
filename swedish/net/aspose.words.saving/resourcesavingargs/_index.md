---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.ResourceSavingArgs, som förbättrar din dokumentbehandling genom att tillhandahålla viktiga data för ResourceSaving-händelsen.
type: docs
weight: 6360
url: /sv/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

Tillhandahåller data för[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) händelse.

För att lära dig mer, besök[Spara ett dokument](https://docs.aspose.com/words/net/save-a-document/) dokumentationsartikel.

```csharp
public class ResourceSavingArgs
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Hämtar dokumentobjektet som för närvarande sparas. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att en resurs har sparats. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Hämtar eller anger filnamnet (utan sökväg) där resursen ska sparas. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Hämtar eller ställer in den enhetliga resursidentifierare (URI) som används för att referera till resursfilen från dokumentet. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Gör det möjligt att ange strömmen där resursen ska sparas. |

## Anmärkningar

Som standard, när Aspose.Words sparar ett dokument till fast sidformat i HTML eller SVG, sparas varje resurs i en separat fil ( ). Aspose.Words använder dokumentets filnamn och ett unikt nummer för att generera ett unikt filnamn ( ) för varje resurs som finns i dokumentet.

`ResourceSavingArgs` tillåter att omdefiniera hur resursfilnamn genereras eller att helt kringgå sparning av resurser i filer genom att tillhandahålla dina egna strömobjekt.

För att tillämpa din egen logik för att generera resursfilnamn, använd [`ResourceFileName`](./resourcefilename/) egendom.

För att spara resurser i strömmar istället för filer, använd[`ResourceStream`](./resourcestream/) egendom.

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
