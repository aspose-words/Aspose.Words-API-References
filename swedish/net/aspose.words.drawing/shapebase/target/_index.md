---
title: ShapeBase.Target
second_title: Aspose.Words för .NET API Referens
description: ShapeBase fast egendom. Hämtar eller ställer in målramen för formhyperlänken.
type: docs
weight: 480
url: /sv/net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

Hämtar eller ställer in målramen för formhyperlänken.

```csharp
public string Target { get; set; }
```

### Anmärkningar

Standardvärdet är en tom sträng.

### Exempel

Visar hur man infogar en form som innehåller en bild och är också en hyperlänk.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + vänsterklicka på formen i Microsoft Word öppnar ett nytt webbläsarfönster
// och ta oss till hyperlänken i egenskapen "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../shapebase/)
* hopsättning [Aspose.Words](../../../)


