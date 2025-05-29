---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: Aspose.Words for .NET
description: 探索 ShadowFormat Visible 属性。轻松检查格式是否可见，提升文档的外观和清晰度。
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

返回`真的`如果应用于此实例的格式可见。

```csharp
public bool Visible { get; }
```

## 评论

不像[`Clear`](../clear/)，分配`错误的`可见不会清除格式， 它只会隐藏形状效果。

## 例子

展示如何使用形状的阴影格式。

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)
    shape.ShadowFormat.Clear();
```

### 也可以看看

* class [ShadowFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
