---
title: HtmlSaveOptions.TableWidthOutputMode
linktitle: TableWidthOutputMode
articleTitle: TableWidthOutputMode
second_title: Aspose.Words for .NET
description: 使用 HtmlSaveOptions TableWidthOutputMode 优化您的 HTML 导出。控制表格行和单元格宽度，实现无缝的 MHTML 和 EPUB 格式。
type: docs
weight: 480
url: /zh/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

控制如何将表格、行和单元格宽度导出为 HTML、MHTML 或 EPUB。 默认值为All.

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

## 评论

在 HTML 格式中，表格、行和单元格元素 （**&lt;表格&gt;**，**&lt;tr&gt;**，**&lt;th&gt;**，**&lt;td&gt;**) 的宽度可以相对（百分比）或绝对单位指定。 在 Aspose.Words 中的文档中，表格、行和单元格也可以使用相对或绝对单位指定其宽度。

当您使用 Aspose.Words 将文档转换为 HTML 时，您可能希望控制表格、行和单元格宽度的导出方式，以影响生成的文档在可视化代理（例如浏览器或查看器）中的显示方式。

使用此属性作为过滤器，指定导出到目标文档的表格宽度值。例如，如果您要将文档转换为 EPUB 格式，并打算在移动阅读设备上查看该文档，那么您可能希望避免导出绝对宽度值。为此，您需要指定输出模式。RelativeOnly或者None 以便移动设备上的查看者可以布局表格以尽可能适应屏幕的宽度。

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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
