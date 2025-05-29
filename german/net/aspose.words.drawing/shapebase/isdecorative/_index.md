---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words für .NET
description: Entdecken Sie ShapeBase. Verwalten Sie dekorative Eigenschaften in Ihren Dokumenten ganz einfach. Verbessern Sie die visuelle Attraktivität, indem Sie Markierungen für einzigartige Formdesigns setzen.
type: docs
weight: 260
url: /de/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Ruft das Flag ab oder legt es fest, das angibt, ob die Form im Dokument dekorativ ist.

```csharp
public bool IsDecorative { get; set; }
```

## Bemerkungen

Beachten Sie, dass die Form nicht leer ist[`AlternativeText`](../alternativetext/) kann nicht dekorativ sein.

## Beispiele

Zeigt, wie man festlegt, dass die Form dekorativ ist.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// Wenn „AlternativeText“ nicht leer ist, kann die Form nicht dekorativ sein.
// Aus diesem Grund hat sich unser Wert auf „false“ geändert.
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// Erstellen Sie eine neue Form als Dekoration.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
