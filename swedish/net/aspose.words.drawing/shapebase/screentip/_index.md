---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase ScreenTip-egenskapen och förbättra användarupplevelsen genom att anpassa verktygstipstexten som visas när muspekaren förs över former.
type: docs
weight: 510
url: /sv/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Definierar texten som visas när muspekaren flyttas över formen.

```csharp
public string ScreenTip { get; set; }
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
