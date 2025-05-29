---
title: ShadowFormat.Color
linktitle: Color
articleTitle: Color
second_title: .NET için Aspose.Words
description: Tasarımlarınızdaki gölge renklerini özelleştirmek için ShadowFormat Color özelliğini keşfedin. Varsayılan Siyah'tır, ancak canlı seçeneklerle yaratıcılığınızı serbest bırakın!
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/shadowformat/color/
---
## ShadowFormat.Color property

Bir tane alırColor gölgenin rengini temsil eden nesne. Varsayılan değerBlack .

```csharp
public Color Color { get; }
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

* class [ShadowFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
