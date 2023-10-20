---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: Aspose.Words för .NET
description: HtmlSaveOptions ExportFontResources fast egendom. Anger om teckensnittsresurser ska exporteras till HTML MHTML eller EPUB. Standard ärfalsk  i C#.
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

Att exportera teckensnittsresurser möjliggör konsekvent dokumentåtergivning oberoende av de teckensnitt som är tillgängliga i en given användares miljö.

Om`ExportFontResources` är satt till`Sann` , kommer huvud-HTML-dokumentet att referera till varje typsnitt via CSS 3**@font-face** at-rule och typsnitt kommer att matas ut som separata filer. Vid export till IDPF EPUB- eller MHTML -format kommer teckensnitt att bäddas in i motsvarande paket tillsammans med andra underordnade filer.

Om[`ExportFontsAsBase64`](../exportfontsasbase64/) är satt till`Sann` kommer teckensnitt inte att sparas i separata filer. Istället kommer de att bäddas in i**@font-face** at-regler i Base64-kodning.

**Viktig!** När du exporterar teckensnittsresurser bör teckensnittslicensproblem övervägas. Författare som vill använda specifika typsnitt via en nedladdningsbar teckensnittsmekanism måste alltid noggrant verifiera att deras avsedda användning ligger inom ramen för teckensnittslicensen. Många kommersiella typsnitt tillåter för närvarande inte webbnedladdning av deras typsnitt i någon form. Licensavtal som täcker vissa typsnitt noterar specifikt att användning via**@font-face** rules i CSS-formatmallar är inte tillåtet. Teckensnittsunderinställningar kan också bryta mot licensvillkoren.

## Exempel

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

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
