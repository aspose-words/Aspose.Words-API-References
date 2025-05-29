---
title: TextDmlEffect Enum
linktitle: TextDmlEffect
articleTitle: TextDmlEffect
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.TextDmlEffect enum för att förbättra textkörningar med dynamiska DML-effekter. Förbättra din dokumentpresentation utan ansträngning!
type: docs
weight: 7260
url: /sv/net/aspose.words/textdmleffect/
---
## TextDmlEffect enumeration

Dml-texteffekt för textkörningar.

```csharp
public enum TextDmlEffect
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Glow | `0` | Glödeffekt, där en suddig färgkontur läggs till utanför objektets kanter. |
| Fill | `1` | Fyllningsöverläggseffekt. |
| Shadow | `2` | Skuggeffekt. |
| Outline | `3` | Kontureffekt. |
| Effect3D | `4` | 3D-effekt. |
| Reflection | `5` | Reflektionseffekt. |

## Exempel

Visar hur man kontrollerar om en körning visar en DrawingML-texteffekt.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
