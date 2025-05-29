---
title: ShadowFormat.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShadowFormat-Type-Eigenschaft, um Ihre Schatteneffekte einfach anzupassen. Rufen Sie den ShadowType ab oder legen Sie ihn fest, um mehr Gestaltungsflexibilität zu erhalten.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/shadowformat/type/
---
## ShadowFormat.Type property

Ruft ab oder setzt die angegebene[`ShadowType`](../../shadowtype/) für ShadowFormat.

```csharp
public ShadowType Type { get; set; }
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

* enum [ShadowType](../../shadowtype/)
* class [ShadowFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
