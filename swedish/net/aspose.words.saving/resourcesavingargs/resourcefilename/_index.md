---
title: ResourceSavingArgs.ResourceFileName
linktitle: ResourceFileName
articleTitle: ResourceFileName
second_title: Aspose.Words för .NET
description: Hantera dina resurser effektivt med ResourceSavingArgs. Ange eller hämta enkelt filnamnet för att spara resurser utan krångel med sökvägar.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

Hämtar eller anger filnamnet (utan sökväg) där resursen ska sparas.

```csharp
public string ResourceFileName { get; set; }
```

## Anmärkningar

Den här egenskapen låter dig omdefiniera hur resursfilnamnen genereras vid export till fast sid-HTML eller SVG.

När händelsen utlöses innehåller den här egenskapen filnamnet som genererades av Aspose.Words. Du kan ändra värdet på den här egenskapen för att spara resursen i en annan fil. Observera att filnamn måste vara unika.

Aspose.Words genererar automatiskt ett unikt filnamn för varje resurs vid export till fast sidformat i HTML- eller SVG-format. Hur resursfilnamnet genereras beror på om du sparar dokumentet till en fil eller en ström.

När man sparar ett dokument till en fil ser det genererade resursfilnamnet ut så här: &lt;dokumentets basfilnamn&gt;.&lt;bildnummer&gt;.&lt;filändelse&gt;.

När man sparar ett dokument i en ström ser det genererade resursfilnamnet ut som Aspose.Words.&lt;dokumentguide&gt;.&lt;bildnummer&gt;.&lt;tillägg&gt;.

`ResourceFileName` måste endast innehålla filnamnet utan sökvägen. Aspose.Words bestämmer sökvägen för att spara och värdet för`källa` attribut för att skriva till fast sida HTML eller SVG med hjälp av dokumentets filnamn,[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) eller[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/) och[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) eller[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/) egenskaper.

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
