---
title: ShadowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShadowFormat-Farbeigenschaft, um die Schattenfarben in Ihren Designs anzupassen. Die Standardeinstellung ist Schwarz, aber lassen Sie Ihrer Kreativität mit lebendigen Optionen freien Lauf!
type: docs
weight: 10
url: /de/net/aspose.words.drawing/shadowformat/color/
---
## ShadowFormat.Color property

Erhält eineColor Objekt, das die Farbe für den Schatten darstellt. Der Standardwert istBlack .

```csharp
public Color Color { get; }
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

* class [ShadowFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
