---
title: HtmlFixedSaveOptions.FontFormat
second_title: Aspose.Words för .NET API Referens
description: HtmlFixedSaveOptions fast egendom. Hämtar eller sätterExportFontFormat används för teckensnittsexport. Standardvärdet ärWoff .
type: docs
weight: 90
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/fontformat/
---
## HtmlFixedSaveOptions.FontFormat property

Hämtar eller sätter[`ExportFontFormat`](../../exportfontformat/) används för teckensnittsexport. Standardvärdet ärWoff .

```csharp
public ExportFontFormat FontFormat { get; set; }
```

### Exempel

Visar hur teckensnitt endast används från målmaskinen när du sparar ett dokument i HTML.

```csharp
Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = true,
    UseTargetMachineFonts = useTargetMachineFonts,
    FontFormat = ExportFontFormat.Ttf,
    ExportEmbeddedFonts = false,
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
    Assert.False(Regex.Match(outDocContents, "@font-face").Success);
else
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success);
```

### Se även

* enum [ExportFontFormat](../../exportfontformat/)
* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* hopsättning [Aspose.Words](../../../)


