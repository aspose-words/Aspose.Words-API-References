---
title: ShapeBase.AspectRatioLocked
second_title: Aspose.Words for .NET API 参考
description: ShapeBase 财产. 指定是否锁定形状的纵横比
type: docs
weight: 40
url: /zh/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

指定是否锁定形状的纵横比。

```csharp
public bool AspectRatioLocked { get; set; }
```

### 评论

默认值取决于[`ShapeType`](../../shapetype/)， 为了Image这是`真的` 但对于其他形状类型来说是`错误的`。

仅对顶级形状有效。

### 例子

展示如何锁定/解锁形状的纵横比。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个形状。如果我们在 Microsoft Word 中打开此文档，我们可以左键单击形状以显示
// 其周边有八个大小调整手柄，我们可以单击并拖动它们来更改其大小。
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// 将“AspectRatioLocked”属性设置为“true”以保留形状的纵横比
// 当使用四个对角线大小调整手柄中的任何一个时，它会更改图像的高度和宽度。
// 使用任何改变高度或宽度的正交尺寸调整手柄仍然会改变纵横比。
// 将“AspectRatioLocked”属性设置为“false”以允许我们
// 使用所有大小调整手柄自由更改图像的纵横比。
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../shapebase/)
* 部件 [Aspose.Words](../../../)


