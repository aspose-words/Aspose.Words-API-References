---
title: GlowFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: 使用我们高效的 GlowFormat Remove 方法，轻松从父对象中移除 GlowFormat。立即提升您的设计工作流程！
type: docs
weight: 40
url: /zh/net/aspose.words.drawing/glowformat/remove/
---
## GlowFormat.Remove method

删除[`GlowFormat`](../)来自父对象。

```csharp
public void Remove()
```

## 例子

展示如何与辉光形状效果进行交互。

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Glow.Color = Color.Salmon;
shape.Glow.Radius = 30;
shape.Glow.Transparency = 0.15;

doc.Save(ArtifactsDir + "Shape.Glow.docx");

doc = new Document(ArtifactsDir + "Shape.Glow.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(Color.FromArgb(217, 250, 128, 114).ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(30, shape.Glow.Radius);
Assert.AreEqual(0.15d, shape.Glow.Transparency, 0.01d);

shape.Glow.Remove();

Assert.AreEqual(Color.Black.ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(0, shape.Glow.Radius);
Assert.AreEqual(0, shape.Glow.Transparency);
```

### 也可以看看

* class [GlowFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
