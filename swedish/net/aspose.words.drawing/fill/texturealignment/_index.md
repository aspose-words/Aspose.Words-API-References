---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words för .NET
description: Ställ in egenskapen TextureAlignment för att optimera kakeltexturfyllningen. Anpassa enkelt justeringen för förbättrad visuell tilltalande och designprecision.
type: docs
weight: 190
url: /sv/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Hämtar eller ställer in justeringen för fyllning av kakeltextur.

```csharp
public TextureAlignment TextureAlignment { get; set; }
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

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
