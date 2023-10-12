---
title: FontSavingArgs.OriginalFileName
second_title: Aspose.Words för .NET API Referens
description: FontSavingArgs fast egendom. Hämtar det ursprungliga teckensnittsfilnamnet med ett tillägg.
type: docs
weight: 100
url: /sv/net/aspose.words.saving/fontsavingargs/originalfilename/
---
## FontSavingArgs.OriginalFileName property

Hämtar det ursprungliga teckensnittsfilnamnet med ett tillägg.

```csharp
public string OriginalFileName { get; }
```

### Anmärkningar

Den här egenskapen innehåller det ursprungliga filnamnet för det aktuella teckensnittet om det är känt. Annars kan det vara en tom sträng.

### Exempel

Visar hur man definierar anpassad logik för att exportera teckensnitt när man sparar till HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Konfigurera ett SaveOptions-objekt för att exportera teckensnitt till separata filer.
    // Ställ in en återuppringning som kommer att hantera teckensnittssparande på ett anpassat sätt.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // Återuppringningen kommer att exportera .ttf-filer och spara dem tillsammans med utdatadokumentet.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// Skriver ut information om exporterade teckensnitt och sparar dem i samma lokala systemmapp som deras utdata .html.
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
        // 1 - Spara den på en lokal filsystemsplats:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - Spara det i en stream:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Se även

* class [FontSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../fontsavingargs/)
* hopsättning [Aspose.Words](../../../)


