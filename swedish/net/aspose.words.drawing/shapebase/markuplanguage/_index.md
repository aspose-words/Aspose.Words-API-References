---
title: ShapeBase.MarkupLanguage
linktitle: MarkupLanguage
articleTitle: MarkupLanguage
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase MarkupLanguage-egenskapen för förbättrad hantering av grafiska objekt. Få tillgång till sömlös integration och förbättrad designeffektivitet idag!
type: docs
weight: 410
url: /sv/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

Hämtar MarkupLanguage som används för detta grafikobjekt.

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
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

* enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
