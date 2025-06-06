---
title: EmbeddedFontFormat Enum
linktitle: EmbeddedFontFormat
articleTitle: EmbeddedFontFormat
second_title: Aspose.Words för .NET
description: Upptäck enum-funktionen Aspose.Words.EmbeddedFontFormat, som definierar formaten för inbäddade teckensnitt i FontInfo-objektet för förbättrad dokumentformatering.
type: docs
weight: 3260
url: /sv/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

Anger formatet för ett visst inbäddat teckensnitt inuti[`FontInfo`](../fontinfo/) objekt.

När man sparar ett dokument till en fil skrivs endast inbäddade teckensnitt i motsvarande format ner.

```csharp
public enum EmbeddedFontFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| EmbeddedOpenType | `0` | Anger EOT-filformatet (Embed OpenType). |
| OpenType | `1` | Anger teckensnitt, inbäddat som en vanlig kopia av OpenType-teckensnittsfilen (TrueType). |

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
