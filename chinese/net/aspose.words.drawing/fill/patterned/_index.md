---
title: Fill.Patterned
second_title: Aspose.Words for .NET API 参考
description: Fill 方法. 将指定填充设置为图案
type: docs
weight: 230
url: /zh/net/aspose.words.drawing/fill/patterned/
---
## Patterned(PatternType) {#patterned}

将指定填充设置为图案。

```csharp
public void Patterned(PatternType patternType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

### 例子

展示如何设置形状的图案。

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// 有多种方法指定填充模式。
// 1 - 将图案应用于形状填充：
fill.Patterned(PatternType.DiagonalBrick);

// 2 - 将具有前景色和背景色的图案应用于形状填充：
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### 也可以看看

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../fill/)
* 部件 [Aspose.Words](../../../)

---

## Patterned(PatternType, Color, Color) {#patterned_1}

将指定填充设置为图案。

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | 前景填充的颜色。 |
| backColor | Color | 背景填充的颜色。 |

### 例子

展示如何设置形状的图案。

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// 有多种方法指定填充模式。
// 1 - 将图案应用于形状填充：
fill.Patterned(PatternType.DiagonalBrick);

// 2 - 将具有前景色和背景色的图案应用于形状填充：
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### 也可以看看

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../fill/)
* 部件 [Aspose.Words](../../../)


