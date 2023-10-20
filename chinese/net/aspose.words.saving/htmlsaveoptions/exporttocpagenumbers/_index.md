---
title: HtmlSaveOptions.ExportTocPageNumbers
linktitle: ExportTocPageNumbers
articleTitle: ExportTocPageNumbers
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions ExportTocPageNumbers 财产. 指定在保存 HTMLMHTML 和 EPUB 时是否将页码写入目录 默认值为错误的 在 C#.
type: docs
weight: 270
url: /zh/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

指定在保存 HTML、MHTML 和 EPUB 时是否将页码写入目录。 默认值为`错误的`.

```csharp
public bool ExportTocPageNumbers { get; set; }
```

## 例子

显示将带有目录的文档保存为 .html 时如何显示页码。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入目录，然后用“标题”格式化的段落填充文档
// 目录将作为条目选取的样式。每个条目将在左侧显示标题段落，
// 以及包含右侧标题的页码。
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 1");
builder.Writeln("Entry 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 3");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 4");
fieldToc.UpdatePageNumbers();
doc.UpdateFields();

// HTML 文档没有页面。如果我们将此文档保存为 HTML，
// 我们的 TOC 显示的页码将没有任何意义。
// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象以从 TOC 中省略这些页码。
// 如果我们将“ExportTocPageNumbers”标志设置为“true”，
// 每个目录条目将显示标题、分隔符和页码，并保留其在 Microsoft Word 中的外观。
// 如果我们将“ExportTocPageNumbers”标志设置为“false”，
// 保存操作将省略分隔符和页码，并保持每个条目的标题不变。
HtmlSaveOptions options = new HtmlSaveOptions { ExportTocPageNumbers = exportTocPageNumbers };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 1</span>" +
        "<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
        "-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
        "<span>2</span>" +
        "</p>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 1</span>" +
        "</p>"));
}
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
