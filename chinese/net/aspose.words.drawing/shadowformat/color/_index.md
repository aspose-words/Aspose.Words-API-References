---
title: ShadowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: 探索 ShadowFormat Color 属性，自定义设计中的阴影颜色。默认颜色为黑色，但您也可以使用多种鲜艳的选项，释放您的创造力！
type: docs
weight: 10
url: /zh/net/aspose.words.drawing/shadowformat/color/
---
## ShadowFormat.Color property

获得Color表示阴影颜色的对象。 默认值为Black.

```csharp
public Color Color { get; }
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

* class [ShadowFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
