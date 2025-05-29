---
title: ShadowFormat.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: Gölge efektlerinizi kolayca özelleştirmek için ShadowFormat Type özelliğini keşfedin. Gelişmiş tasarım esnekliği için ShadowType'ı edinin veya ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/shadowformat/type/
---
## ShadowFormat.Type property

Belirtilen değeri alır veya ayarlar[`ShadowType`](../../shadowtype/) ShadowFormat. için

```csharp
public ShadowType Type { get; set; }
```

## Örnekler

Gölge renginin nasıl elde edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Ayrıca bakınız

* enum [ShadowType](../../shadowtype/)
* class [ShadowFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
