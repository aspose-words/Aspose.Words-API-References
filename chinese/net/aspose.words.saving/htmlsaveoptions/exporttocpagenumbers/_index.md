---
title: HtmlSaveOptions.ExportTocPageNumbers
linktitle: ExportTocPageNumbers
articleTitle: ExportTocPageNumbers
second_title: Aspose.Words for .NET
description: 使用 HtmlSaveOptions 控制 HTML、MHTML 和 EPUB 导出中的目录页码。轻松提升导航和用户体验！
type: docs
weight: 270
url: /zh/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

指定保存 HTML、MHTML 和 EPUB 时是否将页码写入目录。 默认值为`错误的`.

```csharp
public bool ExportTocPageNumbers { get; set; }
```

## 例子

展示将带有目录的文档保存为 .html 时如何显示页码。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入目录，然后使用“标题”格式的段落填充文档
// 目录将作为条目选择的样式。每个条目将在左侧显示标题段落，
// 以及右侧包含标题的页码。
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
// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象来从目录中省略这些页码。
// 如果我们将“ExportTocPageNumbers”标志设置为“true”，
// 每个目录条目将显示标题、分隔符和页码，并保留其在 Microsoft Word 中的外观。
// 如果我们将“ExportTocPageNumbers”标志设置为“false”，
// 保存操作将省略分隔符和页码，并保留每个条目的标题不变。
HtmlSaveOptions options = new HtmlSaveOptions { ExportTocPageNumbers = exportTocPageNumbers };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    Assert.True(outDocContents.Contains(
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
        "<span>Entry 2</span>" +
        "</p>"));
}
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
