---
title: ShapeBase.SoftEdge
linktitle: SoftEdge
articleTitle: SoftEdge
second_title: Aspose.Words for .NET
description: 使用 ShapeBase SoftEdge 增强您的设计，打造流畅柔和的边缘格式。轻松提升视觉效果，在每个项目中脱颖而出！
type: docs
weight: 550
url: /zh/net/aspose.words.drawing/shapebase/softedge/
---
## ShapeBase.SoftEdge property

获取形状的软边缘格式。

```csharp
public SoftEdgeFormat SoftEdge { get; }
```

## 例子

显示如何设置图像分辨率的限制。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

展示如何使用软边缘格式。

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// 将柔和的边缘应用于形状。
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// 加载具有软边缘的矩形文档。
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

// 检查软边缘半径。
Assert.AreEqual(30, softEdgeFormat.Radius);

// 从形状中移除软边缘。
softEdgeFormat.Remove();

// 检查已移除软边缘的半径。
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### 也可以看看

* class [SoftEdgeFormat](../../softedgeformat/)
* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
