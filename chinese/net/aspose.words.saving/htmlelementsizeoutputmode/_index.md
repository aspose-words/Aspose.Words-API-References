---
title: HtmlElementSizeOutputMode Enum
linktitle: HtmlElementSizeOutputMode
articleTitle: HtmlElementSizeOutputMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.HtmlElementSizeOutputMode。控制元素大小以实现最佳的 HTML、MHTML 和 EPUB 导出效果。增强您的文档格式！
type: docs
weight: 5810
url: /zh/net/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enumeration

指定 Aspose.Words 如何将元素宽度和高度导出为 HTML、MHTML 和 EPUB。

```csharp
public enum HtmlElementSizeOutputMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| All | `0` | 文档中指定的所有元素大小（绝对单位和相对单位）均已导出。 |
| RelativeOnly | `1` | 仅当文档中元素尺寸以相对单位指定时，才会导出元素尺寸。 此模式下不导出固定尺寸。可视化代理将计算缺失尺寸，以使 文档布局更自然。 |
| None | `2` | 元素尺寸未导出。可视化代理将根据元素之间的关系自动构建布局。 |

## 例子

展示如何在输出 .html 中保留负缩进。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个带有负缩进的表格，这会将其推到页面左边界的左侧。
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// 插入一个具有正缩进的表格，这会将表格推到右边。
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// 当我们将文档保存为 HTML 时，Aspose.Words 将仅保留负缩进
// 例如，如果我们设置了“AllowNegativeIndent”标志，我们就会将其应用于第一个表
// 在 SaveOptions 对象中我们将传递“true”。
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    AllowNegativeIndent = allowNegativeIndent,
    TableWidthOutputMode = HtmlElementSizeOutputMode.RelativeOnly
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

### 也可以看看

* property [TableWidthOutputMode](../htmlsaveoptions/tablewidthoutputmode/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
