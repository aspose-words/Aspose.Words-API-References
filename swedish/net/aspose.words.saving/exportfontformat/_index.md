---
title: ExportFontFormat Enum
linktitle: ExportFontFormat
articleTitle: ExportFontFormat
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.ExportFontFormat-enum för optimal export av teckensnitt vid rendering till fast HTML-format. Förbättra dokumentets visuella kvalitet!
type: docs
weight: 5740
url: /sv/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

Anger formatet som används för att exportera teckensnitt vid rendering till fast HTML-format.

```csharp
public enum ExportFontFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Woff | `0` | WOFF (webböppet teckensnittsformat). |
| Ttf | `1` | TTF (TrueType-teckensnittsformat). |

## Exempel

Visar hur man endast använder teckensnitt från måldatorn när man sparar ett dokument till HTML.

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

* property [FontFormat](../htmlfixedsaveoptions/fontformat/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
