---
title: ShapeBase.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase SizeInPoints-egenskapen för att enkelt hämta och hantera formmätningar i punkter för exakt designkontroll.
type: docs
weight: 540
url: /sv/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

Hämtar formens storlek i punkter.

```csharp
public SizeF SizeInPoints { get; }
```

## Exempel

Visar hur man verifierar en forms storlek och markupspråk.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
