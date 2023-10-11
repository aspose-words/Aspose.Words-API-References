---
title: Fill.TextureAlignment
second_title: Aspose.Words för .NET API Referens
description: Fill fast egendom. Hämtar eller ställer in justeringen för kakeltexturfyllning.
type: docs
weight: 190
url: /sv/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Hämtar eller ställer in justeringen för kakeltexturfyllning.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

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

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../fill/)
* hopsättning [Aspose.Words](../../../)


