---
title: ShapeBase.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words for .NET
description: 使用 ShapeBase 的 hidden 属性控制形状的可见性。轻松切换可见和隐藏，增强设计灵活性。
type: docs
weight: 230
url: /zh/net/aspose.words.drawing/shapebase/hidden/
---
## ShapeBase.Hidden property

获取或设置一个布尔值，指示形状是否可见。

```csharp
public bool Hidden { get; set; }
```

## 评论

默认值为`错误的`.

## 例子

显示如何隐藏形状。

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
if (!shape.Hidden)
    shape.Hidden = true;

doc.Save(ArtifactsDir + "Shape.Hidden.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
