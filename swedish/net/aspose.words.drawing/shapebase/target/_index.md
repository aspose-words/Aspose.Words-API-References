---
title: ShapeBase.Target
linktitle: Target
articleTitle: Target
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase Target-egenskapen för att enkelt ställa in eller hämta hyperlänkmålramar för dina former, vilket förbättrar användarnavigeringen och upplevelsen.
type: docs
weight: 560
url: /sv/net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

Hämtar eller ställer in målramen för formens hyperlänk.

```csharp
public string Target { get; set; }
```

## Anmärkningar

Standardvärdet är en tom sträng.

## Exempel

Visar hur man infogar en form som innehåller en bild och som också är en hyperlänk.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + vänsterklicka på formen i Microsoft Word öppnar ett nytt webbläsarfönster
// och tar oss till hyperlänken i egenskapen "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
