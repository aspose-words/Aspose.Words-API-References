---
title: BorderType Enum
linktitle: BorderType
articleTitle: BorderType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.BorderType 枚举，获取可自定义的边框选项。通过精确的边框控制和样式增强您的文档！
type: docs
weight: 290
url: /zh/net/aspose.words/bordertype/
---
## BorderType enumeration

指定边框的边。

要了解更多信息，请访问[使用文档进行编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public enum BorderType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `-1` | 默认值. |
| Bottom | `0` | 指定段落或表格单元格的底部边框。 |
| Left | `1` | 指定段落或表格单元格的左边框。 |
| Right | `2` | 指定段落或表格单元格的右边框。 |
| Top | `3` | 指定段落或表格单元格的上边框。 |
| Horizontal | `4` | 指定表格中单元格之间或一致段落之间的水平边框。 |
| Vertical | `5` | 指定表格中单元格之间的垂直边框。 |
| DiagonalDown | `6` | 指定表格单元格的对角边框。 |
| DiagonalUp | `7` | 指定表格单元格的对角边框。 |

## 例子

演示如何插入带有顶部边框的段落。

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
