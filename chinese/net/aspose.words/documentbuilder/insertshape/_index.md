---
title: DocumentBuilder.InsertShape
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 插入指定类型和大小的内联形状
type: docs
weight: 440
url: /zh/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(ShapeType, double, double) {#insertshape_1}

插入指定类型和大小的内联形状。

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| shapeType | ShapeType | 要插入到文档中的形状类型。 |
| width | Double | 形状的宽度（以磅为单位）。 |
| height | Double | 形状的高度（以磅为单位）。 |

### 返回值

插入的形状节点。

### 例子

演示如何将 DML 形状插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是形状可能具有的两种环绕类型。
// 1 - 浮动：
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - 内联：
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// 如果需要创建“非原始”形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
// TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded 或 DiagonalCornersRounded，
// 然后以“严格”或“过渡”合规性保存文档，这允许将形状保存为 DML。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertShape(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertshape}

插入具有指定位置、大小和文本换行类型的自由浮动形状。

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| shapeType | ShapeType | 要插入到文档中的形状类型 |
| horzPos | RelativeHorizontalPosition | 指定从何处测量到形状的水平距离。 |
| left | Double | 从原点到形状左侧的距离（以磅为单位）。 |
| vertPos | RelativeVerticalPosition | 指定从何处测量到形状的垂直距离。 |
| top | Double | 从原点到形状顶边的距离（以磅为单位）。 |
| width | Double | 形状的宽度（以磅为单位）。 |
| height | Double | 形状的宽度（以磅为单位）。 |
| wrapType | WrapType | 指定如何将文本环绕在形状周围。 |

### 返回值

插入的形状节点。

### 例子

演示如何将 DML 形状插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是形状可能具有的两种环绕类型。
// 1 - 浮动：
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - 内联：
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// 如果需要创建“非原始”形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
// TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded 或 DiagonalCornersRounded，
// 然后以“严格”或“过渡”合规性保存文档，这允许将形状保存为 DML。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


