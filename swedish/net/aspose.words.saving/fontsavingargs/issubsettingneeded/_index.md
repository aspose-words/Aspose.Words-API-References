---
title: FontSavingArgs.IsSubsettingNeeded
linktitle: IsSubsettingNeeded
articleTitle: IsSubsettingNeeded
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FontSavingArgs IsSubsettingNeeded för att styra teckensnittsdelinställningar för optimerad export av teckensnittsresurser. Förbättra ditt designarbetsflöde idag!
type: docs
weight: 70
url: /sv/net/aspose.words.saving/fontsavingargs/issubsettingneeded/
---
## FontSavingArgs.IsSubsettingNeeded property

Gör det möjligt att ange om det aktuella teckensnittet ska delmängderas innan export som en teckensnittsresurs.

```csharp
public bool IsSubsettingNeeded { get; set; }
```

## Anmärkningar

Typsnitt kan exporteras som kompletta originaltypsnittsfiler eller delas in i delmängder för att endast inkludera de tecken som används i dokumentet. Delmängder gör det möjligt att minska den resulterande storleken på typsnittsresursen.

Som standard avgör Aspose.Words om delmängder ska utföras eller inte genom att jämföra den ursprungliga teckensnittsfilstorleken med den som anges i[`FontResourcesSubsettingSizeThreshold`](../../htmlsaveoptions/fontresourcessubsettingsizethreshold/) . Du kan åsidosätta detta beteende för enskilda teckensnitt genom att ställa in`IsSubsettingNeeded` egendom.

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
