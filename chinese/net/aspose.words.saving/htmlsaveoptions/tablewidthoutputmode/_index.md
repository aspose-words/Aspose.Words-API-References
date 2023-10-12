---
title: HtmlSaveOptions.TableWidthOutputMode
second_title: Aspose.Words for .NET API 参考
description: HtmlSaveOptions 财产. 控制如何将表格行和单元格宽度导出为 HTMLMHTML 或 EPUB 默认值为All.
type: docs
weight: 460
url: /zh/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

控制如何将表格、行和单元格宽度导出为 HTML、MHTML 或 EPUB。 默认值为All.

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

### 评论

在 HTML 格式中，表格、行和单元格元素 ( **&lt;表&gt;**, **&lt;tr&gt;**, **&lt;第&gt;**, **&lt;td&gt;**) 可以以相对（百分比）或绝对单位指定其宽度。 在 Aspose.Words 的文档中，表格、行和单元格也可以使用相对或绝对单位指定 宽度。

当您使用Aspose.Words 将文档转换为HTML 时，您可能想要控制如何导出 表、行和单元格宽度，以影响生成的文档在可视化代理（例如浏览器或查看器）中的显示 方式。

使用此属性作为过滤器来指定导出到目标文档中的表格宽度值。 例如，如果您要将文档转换为 EPUB 并打算在移动阅读设备上查看该文档， 那么您可能希望避免导出绝对宽度值。为此，您需要指定 输出模式RelativeOnly或者None 以便移动设备上的查看者可以布局表格以尽可能适合屏幕宽度。

### 例子

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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlsaveoptions/)
* 部件 [Aspose.Words](../../../)


