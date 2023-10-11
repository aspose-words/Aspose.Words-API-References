---
title: Class BorderCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.BorderCollection 班级. 的集合Border对象.
type: docs
weight: 90
url: /zh/net/aspose.words/bordercollection/
---
## BorderCollection class

的集合[`Border`](../border/)对象.

要了解更多信息，请访问[使用文档编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | 获取底部边框。 |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | 获取或设置边框颜色。 |
| [Count](../../aspose.words/bordercollection/count/) { get; } | 获取集合中的边框数。 |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | 获取或设置文本边框的距离（以磅为单位）。 |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | 获取在单元格或一致段落之间使用的水平边框。 |
| [Item](../../aspose.words/bordercollection/item/) { get; } | 检索[`Border`](../border/)按边框类型划分的对象。 (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | 获取左边框。 |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | 获取或设置边框样式。 |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | 获取或设置边框宽度（以磅为单位）。 |
| [Right](../../aspose.words/bordercollection/right/) { get; } | 获取右边框。 |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | 获取或设置一个值，指示边框是否有阴影。 |
| [Top](../../aspose.words/bordercollection/top/) { get; } | 获取顶部边框。 |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | 获取单元格之间使用的垂直边框。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | 删除对象的所有边框。 |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(BorderCollection) | 比较边框集合。 |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有边框。 |

### 评论

不同的文档元素具有不同的边框。 例如，[`ParagraphFormat`](../paragraphformat/)有[`Bottom`](./bottom/),[`Left`](./left/),[`Right`](./right/)和[`Top`](./top/)边框。 您可以为每个边框单独指定不同的格式，或者 枚举所有边框并应用相同的格式。

### 例子

演示如何插入带有上边框的段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// 仅当设置了 LineWidth 或 LineStyle 时才设置 ThemeColor。
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### 也可以看看

* class [Border](../border/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


