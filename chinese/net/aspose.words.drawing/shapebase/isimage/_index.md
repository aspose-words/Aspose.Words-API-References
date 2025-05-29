---
title: ShapeBase.IsImage
linktitle: IsImage
articleTitle: IsImage
second_title: Aspose.Words for .NET
description: 使用 ShapeBase 的 IsImage 属性判断形状是否为图像。轻松识别图像形状，增强设计灵活性和功能性。
type: docs
weight: 300
url: /zh/net/aspose.words.drawing/shapebase/isimage/
---
## ShapeBase.IsImage property

返回`真的`如果此形状是图像形状。

```csharp
public bool IsImage { get; }
```

## 例子

展示如何使用基本 URI 从流中打开包含图像的 HTML 文档。

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // 加载时传递基本文件夹的 URI
    // 这样就可以找到 HTML 文档中具有相对 URI 的任何图像。
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // 验证文档的第一个形状是否包含有效的图像。
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
