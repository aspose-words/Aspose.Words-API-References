---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
linktitle: ExportEmbeddedFonts
articleTitle: ExportEmbeddedFonts
second_title: Aspose.Words för .NET
description: Styr inbäddning av teckensnitt i din HTML med egenskapen ExportEmbeddedFonts. Förbättra dokumentkvaliteten samtidigt som du hanterar filstorleken effektivt.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

Anger om teckensnitt ska bäddas in i HTML-dokument i Base64-format. Observera att om du ställer in den här flaggan kan storleken på HTML-utdatafilen ökas avsevärt.

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

## Exempel

Visar hur man avgör var inbäddade teckensnitt ska lagras när man exporterar ett dokument till HTML.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// När vi exporterar ett dokument med inbäddade teckensnitt till .html,
// Aspose.Words kan placera typsnitten på två möjliga platser.
// Om flaggan "ExportEmbeddedFonts" sätts till "true" lagras rådata för inbäddade teckensnitt i CSS-stilarket,
// i egenskapen "url" i regeln "@font-face". Detta kan skapa en enorm CSS-stilarksfil
// och minska antalet externa filer som denna HTML-konvertering kommer att skapa.
// Om denna flagga sätts till "false" skapas en fil för varje typsnitt.
// CSS-stilarket länkar till varje typsnittsfil med hjälp av egenskapen "url" i regeln "@font-face".
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
