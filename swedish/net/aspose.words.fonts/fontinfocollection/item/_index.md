---
title: FontInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FontInfoCollection Item för att enkelt hämta teckensnitt efter namn och förbättra dina designprojekt med precision och stil.
type: docs
weight: 40
url: /sv/net/aspose.words.fonts/fontinfocollection/item/
---
## FontInfoCollection indexer (1 of 2)

Hämtar ett teckensnitt med det angivna namnet.

```csharp
public FontInfo this[string name] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| name | Skiftlägeskänsligt namn på teckensnittet som ska hittas. |

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

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)

---

## FontInfoCollection indexer (2 of 2)

Hämtar ett teckensnitt vid det angivna indexet.

```csharp
public FontInfo this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Nollbaserat index för teckensnittet. |

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

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
