---
title: ShapeBase.ShadowFormat
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: .NET için Aspose.Words
description: Şekiller için özelleştirilebilir gölge efektleriyle tasarımlarınızı geliştirmek için ShapeBase ShadowFormat özelliğini keşfedin. Görsel çekiciliğinizi bugün yükseltin!
type: docs
weight: 520
url: /tr/net/aspose.words.drawing/shapebase/shadowformat/
---
## ShapeBase.ShadowFormat property

Şekil için gölge biçimlendirmesi alır.

```csharp
public ShadowFormat ShadowFormat { get; }
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

* class [ShadowFormat](../../shadowformat/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
