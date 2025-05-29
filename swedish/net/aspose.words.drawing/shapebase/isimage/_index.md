---
title: ShapeBase.IsImage
linktitle: IsImage
articleTitle: IsImage
second_title: Aspose.Words för .NET
description: Upptäck om en form är en bild med ShapeBases IsImage-egenskap. Identifiera enkelt bildformer för förbättrad designflexibilitet och funktionalitet.
type: docs
weight: 300
url: /sv/net/aspose.words.drawing/shapebase/isimage/
---
## ShapeBase.IsImage property

Returer`sann` om den här formen är en bildform.

```csharp
public bool IsImage { get; }
```

## Exempel

Visar hur man öppnar ett HTML-dokument med bilder från en ström med hjälp av en bas-URI.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Skicka URI:n för basmappen när den laddas
    // så att alla bilder med relativa URI:er i HTML-dokumentet kan hittas.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifiera att dokumentets första form innehåller en giltig bild.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
