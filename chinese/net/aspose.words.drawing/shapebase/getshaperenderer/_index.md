---
title: ShapeBase.GetShapeRenderer
linktitle: GetShapeRenderer
articleTitle: GetShapeRenderer
second_title: Aspose.Words for .NET
description: 探索 ShapeBase GetShapeRenderer 方法，轻松创建和渲染形状作为图像，轻松增强您的设计项目。
type: docs
weight: 670
url: /zh/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

创建并返回可用于将此形状渲染为图像的对象。

```csharp
public ShapeRenderer GetShapeRenderer()
```

### 返回值

此形状的渲染器对象。

## 评论

此方法仅调用[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/)构造函数并将 此对象作为参数传递。

## 例子

展示如何使用形状渲染器将形状导出到本地文件系统中的文件。

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// 文档中有 7 个形状，包括一个组形状和 2 个子形状。
// 我们将把每个形状渲染到本地文件系统中的图像文件中
// 同时忽略组形状，因为它们没有外观。
// 这将生成 6 个图像文件。
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### 也可以看看

* class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
