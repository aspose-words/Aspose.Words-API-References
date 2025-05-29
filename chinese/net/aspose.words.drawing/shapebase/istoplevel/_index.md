---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: Aspose.Words for .NET
description: 发现 ShapeBase IsTopLevel。快速验证形状是否独立，并通过高效的群组管理增强您的设计工作流程。
type: docs
weight: 370
url: /zh/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

返回`真的`如果此形状不是组形状的子形状。

```csharp
public bool IsTopLevel { get; }
```

## 例子

展示如何判断一个形状是否是组形状的一部分。

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// 默认情况下，形状不属于任何组形状的一部分，因此“IsTopLevel”属性设置为“true”。
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// 一旦我们将一个形状融入到一个组形状中，“IsTopLevel”属性就会变为“false”。
Assert.False(shape.IsTopLevel);
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
