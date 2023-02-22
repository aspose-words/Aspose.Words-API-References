---
title: Class Border
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Border 班级. 表示对象的边框
type: docs
weight: 70
url: /zh/net/aspose.words/border/
---
## Border class

表示对象的边框。

```csharp
public class Border : InternableComplexAttr
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | 获取或设置边框颜色。 |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | 获取或设置边框与文本或页面边缘的距离（以磅为单位）。 |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | 如果 LineStyle 不是 LineStyle.None，则返回 true。 |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | 获取或设置边框样式 |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | 获取或设置以点为单位的边框宽度。 |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | 获取或设置边框是否有阴影的值。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | 将边框属性重置为默认值。 |
| [Equals](../../aspose.words/border/equals/#equals)(Border) | 判断指定边框的值是否与当前边框相等 |
| override [Equals](../../aspose.words/border/equals/#equals_1)(object) | 确定指定对象的值是否与当前对象相等。 |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | 用作此类型的哈希函数。 |

### 评论

边框可以应用于各种文档元素，包括段落、 段落内的文本运行或表格单元格。

### 例子

演示如何将由边框包围的字符串插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

演示如何插入带有上边框的段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### 也可以看看

* class [InternableComplexAttr](../internablecomplexattr/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


