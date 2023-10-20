---
title: HtmlSaveOptions.ExportRoundtripInformation
linktitle: ExportRoundtripInformation
articleTitle: ExportRoundtripInformation
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions ExportRoundtripInformation 财产. 指定保存为 HTMLMHTML 或 EPUB 时是否写入往返信息 默认值为真的对于 HTML 和错误的对于 MHTML 和 EPUB 在 C#.
type: docs
weight: 240
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

指定保存为 HTML、MHTML 或 EPUB 时是否写入往返信息。 默认值为`真的`对于 HTML 和`错误的`对于 MHTML 和 EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

## 评论

保存往返信息允许在 HTML 文档加载回[`Document`](../../../aspose.words/document/)目的。

什么时候`真的`，往返信息导出为相应 HTML 元素的 -aw-* CSS properties 。

什么时候`错误的`, 导致没有往返信息输出到生成的文件中。

## 例子

展示了在转换为 .html 时如何保留隐藏元素。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 将文档转换为 .html 时，一些元素，如隐藏的书签、原始形状位置、
// 或脚注将被删除或转换为纯文本并有效地丢失。
// 使用将 ExportRoundtripInformation 设置为 true 的 HtmlSaveOptions 对象进行保存将保留这些元素。

// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象来确定
// 保存操作如何导出 HTML 不支持或不使用的文档元素，
// 例如隐藏的书签和原始形状位置。
// 如果我们将“ExportRoundtripInformation”标志设置为“true”，保存操作将保留这些元素。
// 如果我们将“ExportRoundTripInformation”标志设置为“false”，保存操作将丢弃这些元素。
// 如果我们打算使用 Aspose.Words 加载保存的 HTML，我们将希望保留这些元素，
// 因为它们可以再次使用。
HtmlSaveOptions options = new HtmlSaveOptions { ExportRoundtripInformation = exportRoundtripInformation };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");
doc = new Document(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    Assert.True(outDocContents.Contains("<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    Assert.True(outDocContents.Contains("<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
        "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" " +
        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number </span>" +
        "<span style=\"-aw-field-start:true\"></span>" +
        "<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
        "<span style=\"-aw-field-separator:true\"></span>" +
        "<span>1</span>" +
        "<span style=\"-aw-field-end:true\"></span>"));

    Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
else
{
    Assert.True(outDocContents.Contains("<div style=\"clear:both\">"));
    Assert.True(outDocContents.Contains("<span>&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number 1</span>"));

    Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
