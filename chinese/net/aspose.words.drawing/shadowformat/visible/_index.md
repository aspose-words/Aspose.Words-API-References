---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: 用于 .NET 的 Aspose.Words
description: ShadowFormat Visible 财产. 返回真的如果应用于此实例的格式可见 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

返回`真的`如果应用于此实例的格式可见。

```csharp
public bool Visible { get; }
```

## 评论

不像[`Clear`](../clear/) 分配`错误的`to Visible 不会清除格式， 它仅隐藏形状效果。

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
