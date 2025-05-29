---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.TextureAlignment-uppräkningen för exakt texturfyllningsjustering. Förbättra dina dokumentdesigner med sömlösa kakelalternativ!
type: docs
weight: 1780
url: /sv/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Anger justeringen för texturfyllningens kakelsättning.

```csharp
public enum TextureAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| TopLeft | `0` | Texturjustering övre vänstra. |
| Top | `1` | Justering av övre textur. |
| TopRight | `2` | Texturjustering övre högra. |
| Left | `3` | Vänster texturjustering. |
| Center | `4` | Centrera texturjustering. |
| Right | `5` | Höger texturjustering. |
| BottomLeft | `6` | Texturjustering längst ner till vänster. |
| Bottom | `7` | Justering av bottentextur. |
| BottomRight | `8` | Texturjustering längst ner till höger. |
| None | `9` | Ingen texturjustering. |

## Exempel

Visar hur man fyller och kaklar texturen inuti formen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Tillämpa texturjustering på formfyllningen.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Använd alternativet compliance för att definiera formen med DML om du vill få "TextureAlignment"
// egenskap efter att dokumentet har sparats.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);

doc = new Document(ArtifactsDir + "Shape.TextureFill.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(TextureAlignment.TopRight, shape.Fill.TextureAlignment);
Assert.AreEqual(PresetTexture.Canvas, shape.Fill.PresetTexture);
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
