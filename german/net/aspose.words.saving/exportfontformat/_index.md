---
title: ExportFontFormat Enum
linktitle: ExportFontFormat
articleTitle: ExportFontFormat
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.ExportFontFormat opsomming. Gibt das Format an das zum Exportieren von Schriftarten beim Rendern in das feste HTMLFormat verwendet wird in C#.
type: docs
weight: 4990
url: /de/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

Gibt das Format an, das zum Exportieren von Schriftarten beim Rendern in das feste HTML-Format verwendet wird.

```csharp
public enum ExportFontFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Woff | `0` | WOFF (Web Open Font Format). |
| Ttf | `1` | TTF (TrueType-Schriftformat). |

## Beispiele

Zeigt, wie beim Speichern eines Dokuments im HTML-Format Schriftarten nur vom Zielcomputer verwendet werden.

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

### Siehe auch

* property [FontFormat](../htmlfixedsaveoptions/fontformat/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
