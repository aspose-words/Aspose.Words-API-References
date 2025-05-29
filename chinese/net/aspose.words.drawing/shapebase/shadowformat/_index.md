---
title: ShapeBase.ShadowFormat
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words for .NET
description: 探索 ShapeBase ShadowFormat 属性，通过自定义形状阴影效果增强您的设计。立即提升您的视觉吸引力！
type: docs
weight: 520
url: /zh/net/aspose.words.drawing/shapebase/shadowformat/
---
## ShapeBase.ShadowFormat property

获取形状的阴影格式。

```csharp
public ShadowFormat ShadowFormat { get; }
```

## 例子

展示如何获取阴影颜色。

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### 也可以看看

* class [ShadowFormat](../../shadowformat/)
* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
