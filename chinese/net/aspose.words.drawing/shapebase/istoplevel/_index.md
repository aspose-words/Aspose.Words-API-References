---
title: ShapeBase.IsTopLevel
second_title: Aspose.Words for .NET API 参考
description: ShapeBase 财产. 返回真的如果此形状不是组形状的子项.
type: docs
weight: 350
url: /zh/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

返回`真的`如果此形状不是组形状的子项.

```csharp
public bool IsTopLevel { get; }
```

### 例子

演示如何判断形状是否是组形状的一部分。

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// 默认情况下，形状不属于任何组形状，因此“IsTopLevel”属性设置为“true”。
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// 一旦我们将形状同化为组形状，“IsTopLevel”属性就会更改为“false”。
Assert.False(shape.IsTopLevel);
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../shapebase/)
* 部件 [Aspose.Words](../../../)


