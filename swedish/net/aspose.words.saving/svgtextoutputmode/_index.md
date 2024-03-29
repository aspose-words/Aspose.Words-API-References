---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words för .NET
description: Aspose.Words.Saving.SvgTextOutputMode uppräkning. Gör det möjligt att ange hur text i ett dokument ska renderas när du sparar i SVGformat i C#.
type: docs
weight: 5610
url: /sv/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Gör det möjligt att ange hur text i ett dokument ska renderas när du sparar i SVG-format.

```csharp
public enum SvgTextOutputMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| UseSvgFonts | `0` | SVG-teckensnitt används för att återge text. Observera att inte alla webbläsare stöder SVG-teckensnitt. |
| UseTargetMachineFonts | `1` | Teckensnitt som är installerade på måldatorn används för att rendera text. Observera att om några teckensnitt som används i dokumentet inte är tillgängliga på måldatorn kan dokumentet se annorlunda ut. |
| UsePlacedGlyphs | `2` | Text renderas med kurvor. Obs, textval fungerar inte om du använder det här alternativet. |

## Exempel

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
