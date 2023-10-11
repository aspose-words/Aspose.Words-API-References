---
title: Enum TextureAlignment
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.TextureAlignment uppräkning. Anger justeringen för plattsättningen av texturfyllningen.
type: docs
weight: 1370
url: /sv/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Anger justeringen för plattsättningen av texturfyllningen.

```csharp
public enum TextureAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| TopLeft | `0` | Texturjustering upptill till vänster. |
| Top | `1` | Toppstrukturjustering. |
| TopRight | `2` | Texturjustering upptill till höger. |
| Left | `3` | Vänster texturjustering. |
| Center | `4` | Centrera texturjustering. |
| Right | `5` | Höger texturjustering. |
| BottomLeft | `6` | Texturjustering längst ned till vänster. |
| Bottom | `7` | Bottenstrukturjustering. |
| BottomRight | `8` | Texturjustering längst ned till höger. |
| None | `9` | Ingen texturjustering. |

### Exempel

Visar hur man fyller och kakelar strukturen inuti formen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Tillämpa texturjustering på formfyllningen.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Använd efterlevnadsalternativet för att definiera formen med DML om du vill få "TextureAlignment"
// egenskap efter att dokumentet har sparats.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)


