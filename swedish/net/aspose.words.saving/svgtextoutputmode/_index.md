---
title: Enum SvgTextOutputMode
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.SvgTextOutputMode uppräkning. 
type: docs
weight: 5330
url: /sv/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

```csharp
public enum SvgTextOutputMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| UseSvgFonts | `0` | SVG-teckensnitt används för att återge text. Observera att inte alla webbläsare stöder SVG-teckensnitt. |
| UseTargetMachineFonts | `1` | Teckensnitt som är installerade på måldatorn används för att rendera text. Observera att om några teckensnitt som används i dokumentet inte är tillgängliga på måldatorn kan dokumentet se annorlunda ut. |
| UsePlacedGlyphs | `2` | Text renderas med kurvor. Obs, textval fungerar inte om du använder det här alternativet. |

### Exempel

Visar hur man efterliknar egenskaperna hos bilder när man konverterar ett .docx-dokument till .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Konfigurera SvgSaveOptions-objektet för att spara utan sidkanter eller valbar text.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


