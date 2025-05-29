---
title: ShadowFormat.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: 探索 ShadowFormat Type 属性，轻松自定义阴影效果。获取或设置 ShadowType 可增强设计灵活性。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/shadowformat/type/
---
## ShadowFormat.Type property

获取或设置指定的[`ShadowType`](../../shadowtype/)对于 ShadowFormat.

```csharp
public ShadowType Type { get; set; }
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

* enum [ShadowType](../../shadowtype/)
* class [ShadowFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
