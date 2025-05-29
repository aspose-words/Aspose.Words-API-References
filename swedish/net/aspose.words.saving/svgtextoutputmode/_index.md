---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.SvgTextOutputMode enum för att anpassa textrendering i SVG-format, vilket förbättrar dokumentpresentationen och den visuella attraktionskraften.
type: docs
weight: 6410
url: /sv/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Gör det möjligt att ange hur text i ett dokument ska återges när det sparas i SVG-format.

```csharp
public enum SvgTextOutputMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| UseSvgFonts | `0` | SVG-teckensnitt används för att rendera text. Observera att inte alla webbläsare stöder SVG-teckensnitt. |
| UseTargetMachineFonts | `1` | Typsnitt som är installerade på måldatorn används för att rendera text. Observera att om vissa av de typsnitt som används i dokumentet inte är tillgängliga på måldatorn kan dokumentet se annorlunda ut. |
| UsePlacedGlyphs | `2` | Texten återges med hjälp av kurvor. Observera att textmarkering inte fungerar om du använder det här alternativet. |

## Exempel

Visar hur man efterliknar bilders egenskaper när man konverterar ett .docx-dokument till .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Konfigurera SvgSaveOptions-objektet för att spara utan sidkantlinjer eller valbar text.
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
