---
title: SoftEdgeFormat Class
linktitle: SoftEdgeFormat
articleTitle: SoftEdgeFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.SoftEdgeFormat 类，使用令人惊叹的柔和边缘效果增强您的文档，使其具有专业外观。
type: docs
weight: 1710
url: /zh/net/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class

表示对象的软边缘格式。

```csharp
public class SoftEdgeFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Radius](../../aspose.words.drawing/softedgeformat/radius/) { get; set; } | 获取或设置一个双精度值，以点 (pt) 为单位表示柔和边缘效果的半径长度。 默认值为 0.0。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Remove](../../aspose.words.drawing/softedgeformat/remove/)() | 删除`SoftEdgeFormat`来自父对象。 |

## 评论

使用[`SoftEdge`](../shapebase/softedge/)属性来访问对象的软边缘属性。 您不创建`SoftEdgeFormat`直接上课。

## 例子

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

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
