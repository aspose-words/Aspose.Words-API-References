---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
linktitle: ExportEmbeddedFonts
articleTitle: ExportEmbeddedFonts
second_title: Aspose.Words för .NET
description: HtmlFixedSaveOptions ExportEmbeddedFonts fast egendom. Anger om teckensnitt ska bäddas in i HTMLdokument i Base64format. Observera att denna flagga kan öka storleken på utdatafilen avsevärt i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

Anger om teckensnitt ska bäddas in i HTML-dokument i Base64-format. Observera att denna flagga kan öka storleken på utdatafilen avsevärt.

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

## Exempel

Visar hur man bestämmer var man ska lagra inbäddade teckensnitt när man exporterar ett dokument till HTML.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// När vi exporterar ett dokument med inbäddade teckensnitt till .html,
// Aspose.Words kan placera typsnitten på två möjliga platser.
// Om du ställer in "ExportEmbeddedFonts"-flaggan till "true" lagras rådata för inbäddade typsnitt i CSS-formatmallen,
// i egenskapen "url" för regeln "@font-face". Detta kan skapa en enorm CSS-formatmallsfil
// och minska antalet externa filer som denna HTML-konvertering kommer att skapa.
// Om du ställer in denna flagga till "false" skapas en fil för varje typsnitt.
// CSS-formatmallen länkar till varje typsnittsfil med "url"-egenskapen för "@font-face"-regeln.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedFonts = exportEmbeddedFonts
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(0, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(2, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
