---
title: ShapeBase.ShadowFormat
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase ShadowFormat-Eigenschaft, um Ihre Designs mit anpassbaren Schatteneffekten für Formen zu verbessern. Steigern Sie noch heute Ihre visuelle Wirkung!
type: docs
weight: 520
url: /de/net/aspose.words.drawing/shapebase/shadowformat/
---
## ShapeBase.ShadowFormat property

Ruft die Schattenformatierung für die Form ab.

```csharp
public ShadowFormat ShadowFormat { get; }
```

## Beispiele

Zeigt, wie man Schattenfarbe erhält.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Siehe auch

* class [ShadowFormat](../../shadowformat/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
