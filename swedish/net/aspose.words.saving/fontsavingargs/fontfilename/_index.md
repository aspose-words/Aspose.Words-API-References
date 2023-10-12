---
title: FontSavingArgs.FontFileName
second_title: Aspose.Words för .NET API Referens
description: FontSavingArgs fast egendom. Hämtar eller ställer in filnamnet utan sökväg där typsnittet ska sparas.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

Hämtar eller ställer in filnamnet (utan sökväg) där typsnittet ska sparas.

```csharp
public string FontFileName { get; set; }
```

### Anmärkningar

Den här egenskapen låter dig omdefiniera hur teckensnittsfilnamnen genereras under export till HTML.

När händelsen aktiveras innehåller den här egenskapen filnamnet som genererades av Aspose.Words. Du kan ändra värdet på den här egenskapen för att spara teckensnittet i en annan fil. Observera att filnamn måste vara unika.

Aspose.Words genererar automatiskt ett unikt filnamn för varje inbäddat typsnitt när exporteras till HTML-format. Hur teckensnittsfilnamnet genereras beror på om du sparar dokumentet till en fil eller i en stream.

När du sparar ett dokument till en fil ser det genererade teckensnittsfilnamnet ut som &lt;dokumentbasfilnamn&gt;.&lt;originalfilnamn&gt;&lt;valfritt suffix&gt;.&lt;tillägg&gt;.

När du sparar ett dokument i en ström ser det genererade teckensnittsfilnamnet ut som Aspose.Words.&lt;dokumentguide&gt;.&lt;originalfilnamn&gt;&lt;valfritt suffix&gt;.&lt;tillägg&gt;.

`FontFileName` måste endast innehålla filnamnet utan sökvägen. Aspose.Words bestämmer sökvägen för att spara med hjälp av dokumentets filnamn, [`FontsFolder`](../../htmlsaveoptions/fontsfolder/) och [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) egenskaper.

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


