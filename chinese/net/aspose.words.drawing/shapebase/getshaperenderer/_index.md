---
title: GetShapeRenderer
second_title: Aspose.Words for .NET API 参考
description: 创建并返回一个可用于将此形状渲染为图像的对象
type: docs
weight: 600
url: /zh/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

创建并返回一个可用于将此形状渲染为图像的对象。

```csharp
public ShapeRenderer GetShapeRenderer()
```

### 返回值

此形状的渲染器对象。

### 评论

这个方法只是调用[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer)构造函数并将 这个对象作为参数传递。

### 例子

演示如何使用形状渲染器将形状导出到本地文件系统中的文件。

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// 文档中有 7 个形状，包括一组形状和 2 个子形状。
// 我们会将每个形状渲染到本地文件系统中的一个图像文件中
// 同时忽略组形状，因为它们没有外观。
// 这将产生 6 个图像文件。
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### 也可以看看

* class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer)
* class [ShapeBase](../../shapebase)
* 命名空间 [Aspose.Words.Drawing](../../shapebase)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->