---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words EmbeddedFontStyle-enum för att enkelt hantera inbäddade teckensnitt i FontInfo-objekt och förbättra dina dokumentformateringsmöjligheter.
type: docs
weight: 3270
url: /sv/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Anger stilen för ett inbäddat teckensnitt inuti en[`FontInfo`](../fontinfo/) objekt.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Regular | `0` | Anger det vanliga inbäddade teckensnittet. |
| Bold | `1` | Anger det inbäddade teckensnittet för fetstil. |
| Italic | `2` | Anger det kursiva inbäddade teckensnittet. |
| BoldItalic | `3` | Anger det inbäddade teckensnittet Fet-Kursiv. |

## Exempel

Visar hur man extraherar ett inbäddat teckensnitt från ett dokument och sparar det i det lokala filsystemet.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Inbäddade teckensnittsformat kan skilja sig i andra format som .doc.
// Vi behöver veta rätt format innan vi kan extrahera teckensnittet.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Vi kan också konvertera inbäddat OpenType-format, som kommer från .doc-dokument, till OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Se även

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
