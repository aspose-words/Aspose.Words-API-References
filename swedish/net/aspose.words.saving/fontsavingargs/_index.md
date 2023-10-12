---
title: Class FontSavingArgs
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.FontSavingArgs klass. Tillhandahåller data förFontSaving händelse.
type: docs
weight: 5030
url: /sv/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Tillhandahåller data för[`FontSaving`](../ifontsavingcallback/fontsaving/) händelse.

För att lära dig mer, besök[Spara ett dokument](https://docs.aspose.com/words/net/save-a-document/) dokumentationsartikel.

```csharp
public class FontSavingArgs
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Indikerar om det aktuella teckensnittet är fetstilt. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Hämtar dokumentobjektet som sparas. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Indikerar det aktuella teckensnittets efternamn. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Hämtar eller ställer in filnamnet (utan sökväg) där typsnittet ska sparas. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Tillåter att ange strömmen där teckensnittet ska sparas. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Tillåter att ange om det aktuella teckensnittet kommer att exporteras som en teckensnittsresurs. Standard är`Sann` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Tillåter att ange om det aktuella teckensnittet kommer att underordnas innan det exporteras som en teckensnittsresurs. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Indikerar om det aktuella teckensnittet är kursivt. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att ha sparat ett teckensnitt. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Hämtar det ursprungliga teckensnittsfilnamnet med ett tillägg. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Får den ursprungliga teckensnittsfilstorleken. |

### Anmärkningar

När Aspose.Words sparar ett dokument till HTML eller relaterade format och[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) är inställd på`Sann`, sparar varje teckensnittsämne för export till en separat fil.

`FontSavingArgs` styr om en viss typsnittsresurs ska exporteras och hur.

`FontSavingArgs`tillåter också att omdefiniera hur teckensnittsfilnamn genereras eller att helt kringgå lagring av teckensnitt i filer genom att tillhandahålla dina egna strömobjekt.

För att bestämma om du vill spara en viss typsnittsresurs, använd[`IsExportNeeded`](./isexportneeded/) fast egendom.

För att spara teckensnitt i strömmar istället för filer, använd[`FontStream`](./fontstream/) fast egendom.

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


