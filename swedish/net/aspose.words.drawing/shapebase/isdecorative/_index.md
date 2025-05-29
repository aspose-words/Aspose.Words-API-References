---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase. Hantera enkelt dekorativa egenskaper i dina dokument. Förbättra det visuella genom att ställa in flaggor för unika formdesigner.
type: docs
weight: 260
url: /sv/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Hämtar eller ställer in flaggan som anger om formen är dekorativ i dokumentet.

```csharp
public bool IsDecorative { get; set; }
```

## Anmärkningar

Observera att formen inte har en tom[`AlternativeText`](../alternativetext/) kan inte vara dekorativ.

## Exempel

Visar hur man ställer in att formen är dekorativ.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// Om "AlternativText" inte är tomt kan formen inte vara dekorativ.
// Det är därför vårt värde har ändrats till 'falskt'.
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// Skapa en ny form som dekoration.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
