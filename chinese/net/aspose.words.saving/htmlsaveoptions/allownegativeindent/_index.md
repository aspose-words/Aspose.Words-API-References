---
title: HtmlSaveOptions.AllowNegativeIndent
linktitle: AllowNegativeIndent
articleTitle: AllowNegativeIndent
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions AllowNegativeIndent 财产. 指定保存为 HTMLMHTML 或 EPUB 时段落的左右负缩进是否标准化 默认值为错误的 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/htmlsaveoptions/allownegativeindent/
---
## HtmlSaveOptions.AllowNegativeIndent property

指定保存为 HTML、MHTML 或 EPUB 时段落的左右负缩进是否标准化 。默认值为`错误的`.

```csharp
public bool AllowNegativeIndent { get; set; }
```

## 评论

当不允许负缩进时，它会以零边距导出到 HTML。 当允许负缩进时，段落可能会部分显示在 浏览器窗口之外。

## 例子

演示如何在输出 .html 中保留负缩进。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个带有负缩进的表格，这会将其推到左侧越过左页边界。
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// 插入一个带有正缩进的表格，这会将表格推到右侧。
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// 当我们将文档保存为 HTML 时，Aspose.Words 将仅保留负缩进
// 例如，如果我们设置“AllowNegativeIndent”标志，我们就将其应用于第一个表
// 在我们将传递给“true”的 SaveOptions 对象中。
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

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
