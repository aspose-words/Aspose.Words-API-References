---
title: Fill.PresetTexture
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words för .NET
description: Upptäck hur du enkelt ställer in egenskapen PresetTexture och förbättrar dina designer med fantastiska fyllningsalternativ. Släpp lös din kreativa potential idag!
type: docs
weight: 170
url: /sv/net/aspose.words.drawing/fill/presettexture/
---
## Fill.PresetTexture property

Får en[`PresetTexture`](../../presettexture/) för fyllningen.

```csharp
public PresetTexture PresetTexture { get; }
```

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

* enum [PresetTexture](../../presettexture/)
* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
