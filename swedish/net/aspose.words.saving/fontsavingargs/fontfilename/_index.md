---
title: FontSavingArgs.FontFileName
linktitle: FontFileName
articleTitle: FontFileName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FontSavingArgs FontFileName, hantera enkelt teckensnittsfilnamn och förbättra ditt designarbetsflöde med sömlösa sparfunktioner.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

Hämtar eller anger filnamnet (utan sökväg) där teckensnittet ska sparas.

```csharp
public string FontFileName { get; set; }
```

## Anmärkningar

Den här egenskapen låter dig omdefiniera hur teckensnittsfilnamnen genereras vid export till HTML.

När händelsen utlöses innehåller den här egenskapen filnamnet som genererades av Aspose.Words. Du kan ändra värdet på den här egenskapen för att spara teckensnittet i en annan fil. Observera att filnamn måste vara unika.

Aspose.Words genererar automatiskt ett unikt filnamn för varje inbäddat teckensnitt när det exporteras till HTML-format. Hur teckensnittsfilnamnet genereras beror på om du sparar dokumentet till en fil eller till en dataström.

När man sparar ett dokument till en fil ser det genererade teckensnittsfilnamnet ut som &lt;dokumentets basfilnamn&gt;.&lt;ursprungligt filnamn&gt;&lt;valfritt suffix&gt;.&lt;filändelse&gt;.

När man sparar ett dokument i en ström ser det genererade teckensnittsfilnamnet ut som Aspose.Words.&lt;dokumentguide&gt;.&lt;ursprungligt filnamn&gt;&lt;valfritt suffix&gt;.&lt;filändelse&gt;.

`FontFileName` måste endast innehålla filnamnet utan sökvägen. Aspose.Words bestämmer sökvägen för att spara med hjälp av dokumentets filnamn, [`FontsFolder`](../../htmlsaveoptions/fontsfolder/) och [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) egenskaper.

## Exempel

Visar hur man definierar anpassad logik för export av teckensnitt när man sparar till HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Konfigurera ett SaveOptions-objekt för att exportera teckensnitt till separata filer.
    // Ställ in en återanropning som hanterar teckensnittssparning på ett anpassat sätt.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // Återanropet exporterar .ttf-filer och sparar dem tillsammans med utdatadokumentet.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// Skriver ut information om exporterade teckensnitt och sparar dem i samma lokala systemmapp som deras utdata-.html.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // Vi kan också komma åt källdokumentet härifrån.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // Det finns två sätt att spara ett exporterat teckensnitt.
        // 1 - Spara det till en lokal filsystemplats:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - Spara det till en ström:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Se även

* class [FontSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
