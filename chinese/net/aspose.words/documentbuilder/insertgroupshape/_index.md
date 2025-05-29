---
title: DocumentBuilder.InsertGroupShape
linktitle: InsertGroupShape
articleTitle: InsertGroupShape
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder 的 InsertGroupShape 方法轻松分组形状。通过无缝插入新的 GroupShape 节点，创建井然有序的设计。
type: docs
weight: 360
url: /zh/net/aspose.words/documentbuilder/insertgroupshape/
---
## InsertGroupShape(*params ShapeBase[]*) {#insertgroupshape}

将作为参数传递的形状分组到插入当前位置的新 GroupShape 节点中。

```csharp
public GroupShape InsertGroupShape(params ShapeBase[] shapes)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| shapes | ShapeBase[] | 要分组的形状列表。 |

## 评论

新 GroupShape 的位置和尺寸将自动计算。

VML 和 DML 形状不能组合在一起。

## 例子

展示如何将组形状与形状结合起来。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// 将形状组合成 GroupShape 节点，并插入到指定位置。
GroupShape groupShape1 = builder.InsertGroupShape(shape1, shape2);

// 组合 Shape 和 GroupShape 节点。
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(groupShape1, shape3);

doc.Save(ArtifactsDir + "Shape.CombineGroupShape.docx");
```

显示如何插入 DML 组形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// 新 GroupShape 节点的尺寸。
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// 插入指定大小的GroupShape节点，该节点插入到指定位置。
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// 插入 GroupShape 节点，其位置和尺寸将自动计算。
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### 也可以看看

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertGroupShape(*double, double, double, double, params ShapeBase[]*) {#insertgroupshape_1}

将作为参数传递的形状分组到指定大小的新 GroupShape 节点中，然后插入到指定位置。

```csharp
public GroupShape InsertGroupShape(double left, double top, double width, double height, 
    params ShapeBase[] shapes)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| left | Double | 从原点到组形状左侧的距离（以点为单位）。 |
| top | Double | 从原点到组形状顶部的距离（以点为单位）。 |
| width | Double | 组形状的宽度（以磅为单位）。不允许使用负值。 |
| height | Double | 组形状的高度（以磅为单位）。不允许使用负值。 |
| shapes | ShapeBase[] | 要分组的形状列表。 |

## 评论

VML 和 DML 形状不能组合在一起。

## 例子

显示如何插入 DML 组形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// 新 GroupShape 节点的尺寸。
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// 插入指定大小的GroupShape节点，该节点插入到指定位置。
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// 插入 GroupShape 节点，其位置和尺寸将自动计算。
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### 也可以看看

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
