---
title: FontInfo.GetEmbeddedFontAsOpenType
linktitle: GetEmbeddedFontAsOpenType
articleTitle: GetEmbeddedFontAsOpenType
second_title: Aspose.Words för .NET
description: Upptäck hur metoden FontInfo GetEmbeddedFontAsOpenType hämtar inbäddade teckensnitt i OpenType-format, vilket förbättrar din designflexibilitet och kvalitet.
type: docs
weight: 100
url: /sv/net/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo.GetEmbeddedFontAsOpenType method

Hämtar en inbäddad typsnittsfil i OpenType-format. Typsnitt i inbäddat OpenType-format konverteras till OpenType.

```csharp
public byte[] GetEmbeddedFontAsOpenType(EmbeddedFontStyle style)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| style | EmbeddedFontStyle | Anger vilket teckensnitt som ska hämtas. |

### Returvärde

Returer`null` om det angivna teckensnittet inte är inbäddat.

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

* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
