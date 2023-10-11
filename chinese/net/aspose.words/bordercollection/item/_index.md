---
title: BorderCollection.Item
second_title: Aspose.Words for .NET API 参考
description: BorderCollection 财产. 检索Border按边框类型划分的对象
type: docs
weight: 60
url: /zh/net/aspose.words/bordercollection/item/
---
## BorderCollection indexer (1 of 2)

检索[`Border`](../../border/)按边框类型划分的对象。

```csharp
public Border this[BorderType borderType] { get; }
```

| 范围 | 描述 |
| --- | --- |
| borderType | A[`BorderType`](../../bordertype/) value 指定要检索的边框的类型。 |

### 评论

请注意，并非所有边框都适用于不同的文档元素。 如果您请求不适用于当前对象的边框，此方法将引发异常。

### 例子

展示如何用边框和底纹装饰文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### 也可以看看

* class [Border](../../border/)
* enum [BorderType](../../bordertype/)
* class [BorderCollection](../)
* 命名空间 [Aspose.Words](../../bordercollection/)
* 部件 [Aspose.Words](../../../)

---

## BorderCollection indexer (2 of 2)

检索[`Border`](../../border/)按索引的对象.

```csharp
public Border this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 要检索的边界的从零开始的索引。 |

### 例子

展示边框集合如何共享元素。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// 因为我们在创建时使用了相同的边框配置
// 这些段落，它们的边框集合共享相同的元素。
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
BorderCollection secondParagraphBorders = builder.CurrentParagraph.ParagraphFormat.Borders;
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsTrue(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());
    Assert.False(firstParagraphBorders[i].IsVisible);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

// 在第二段中更改边框的线条样式后，
// 边界集合不再共享相同的元素。
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // 更改空边框的外观使其可见。
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### 也可以看看

* class [Border](../../border/)
* class [BorderCollection](../)
* 命名空间 [Aspose.Words](../../bordercollection/)
* 部件 [Aspose.Words](../../../)


