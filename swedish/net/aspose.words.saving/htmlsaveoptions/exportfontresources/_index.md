---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlSaveOptions ExportFontResources för att styra export av teckensnittsresurser för HTML, MHTML eller EPUB. Maximera ditt dokuments visuella attraktionskraft!
type: docs
weight: 140
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Anger om teckensnittsresurser ska exporteras till HTML, MHTML eller EPUB. Standard är`falsk` .

```csharp
public bool ExportFontResources { get; set; }
```

## Anmärkningar

Export av teckensnittsresurser möjliggör konsekvent dokumentrendering oberoende av de teckensnitt som är tillgängliga i en given användares miljö.

Om`ExportFontResources` är inställd på`sann` , huvud-HTML-dokumentet kommer att referera till varje typsnitt via CSS 3**@font-face** at-rule och teckensnitt kommer att matas ut som separata filer. Vid export till IDPF EPUB- eller MHTML -format kommer teckensnitt att bäddas in i motsvarande paket tillsammans med andra underfiler.

Om[`ExportFontsAsBase64`](../exportfontsasbase64/) är inställd på`sann` , teckensnitt kommer inte att sparas i separata filer. Istället kommer de att bäddas in i**@font-face** at-regler i Base64-kodning.

**Viktig!**Vid export av typsnittsresurser bör man beakta frågor om typsnittslicenser. Författare som vill använda specifika typsnitt via en nedladdningsbar typsnittsmekanism måste alltid noggrant kontrollera att deras avsedda användning ligger inom typsnittslicensens omfattning. Många kommersiella typsnitt tillåter för närvarande inte nedladdning av deras typsnitt på webben i någon form. Licensavtal som täcker vissa typsnitt noterar specifikt att användning via**@font-face** rules i CSS-stilmallar är inte tillåtet. Delmängder av teckensnitt kan också bryta mot licensvillkoren.

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

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
