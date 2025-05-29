---
title: BorderCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 探索 BorderCollection Item 属性，轻松按类型访问 Border 对象。高效的边框管理，简化您的设计！
type: docs
weight: 60
url: /zh/net/aspose.words/bordercollection/item/
---
## BorderCollection indexer (1 of 2)

检索[`Border`](../../border/)按边框类型划分的对象.

```csharp
public Border this[BorderType borderType] { get; }
```

| 范围 | 描述 |
| --- | --- |
| borderType | 一个[`BorderType`](../../bordertype/)value 指定要检索的边框类型。 |

## 评论

请注意，并非所有边框都适用于不同的文档元素。 如果您请求的边框不适用于当前对象，则此方法会引发异常。

## 例子

展示如何使用边框和阴影装饰文本。

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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## BorderCollection indexer (2 of 2)

检索[`Border`](../../border/)按索引排序的对象.

```csharp
public Border this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 要检索的边框的从零开始的索引。 |

## 例子

展示边界集合如何共享元素。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// 由于我们在创建时使用了相同的边框配置
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

// 仅在第二段中更改边框的线条样式后，
// 边框集合不再共享相同的元素。
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // 改变空边框的外观使其可见。
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### 也可以看看

* class [Border](../../border/)
* class [BorderCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
