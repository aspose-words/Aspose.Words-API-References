---
title: TextEffect Enum
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words för .NET
description: Utforska Aspose.Words.TextEffect-enum för dynamiska textanimationer. Förbättra dina dokument med engagerande effekter för en fängslande användarupplevelse.
type: docs
weight: 7270
url: /sv/net/aspose.words/texteffect/
---
## TextEffect enumeration

Animeringseffekt för textkörningar.

```csharp
public enum TextEffect
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` |  |
| LasVegasLights | `1` |  |
| BlinkingBackground | `2` |  |
| SparkleText | `3` |  |
| MarchingBlackAnts | `4` |  |
| MarchingRedAnts | `5` |  |
| Shimmer | `6` |  |

## Exempel

Visar hur man tillämpar en visuell effekt på en löprunda.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Äldre versioner av Microsoft Word stöder endast teckensnittsanimationseffekter.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
