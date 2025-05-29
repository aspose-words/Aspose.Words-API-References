---
title: ShapeBase.ShadowFormat
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase ShadowFormat-egenskapen för att förbättra dina designer med anpassningsbara skuggeffekter för former. Förhöj din visuella attraktionskraft idag!
type: docs
weight: 520
url: /sv/net/aspose.words.drawing/shapebase/shadowformat/
---
## ShapeBase.ShadowFormat property

Hämtar skuggformatering för formen.

```csharp
public ShadowFormat ShadowFormat { get; }
```

## Exempel

Visar hur man får skuggfärg.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Se även

* class [ShadowFormat](../../shadowformat/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
