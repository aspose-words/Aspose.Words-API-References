---
title: FontInfo.GetEmbeddedFont
linktitle: GetEmbeddedFont
articleTitle: GetEmbeddedFont
second_title: Aspose.Words för .NET
description: FontInfo GetEmbeddedFont metod. Får en specifik inbäddad teckensnittsfil i C#.
type: docs
weight: 80
url: /sv/net/aspose.words.fonts/fontinfo/getembeddedfont/
---
## FontInfo.GetEmbeddedFont method

Får en specifik inbäddad teckensnittsfil.

```csharp
public byte[] GetEmbeddedFont(EmbeddedFontFormat format, EmbeddedFontStyle style)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| format | EmbeddedFontFormat | Anger teckensnittsformatet som ska hämtas. |
| style | EmbeddedFontStyle | Anger typsnittet som ska hämtas. |

### Returvärde

Returnerar`null`om det angivna teckensnittet inte är inbäddat.

## Exempel

Visar hur man extraherar ett inbäddat teckensnitt från ett dokument och sparar det i det lokala filsystemet.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Inbäddade teckensnittsformat kan vara annorlunda i andra format som .doc.
// Vi behöver veta det korrekta formatet innan vi kan extrahera teckensnittet.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Dessutom kan vi konvertera inbäddat OpenType-format, som kommer från .doc-dokument, till OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Se även

* enum [EmbeddedFontFormat](../../embeddedfontformat/)
* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
