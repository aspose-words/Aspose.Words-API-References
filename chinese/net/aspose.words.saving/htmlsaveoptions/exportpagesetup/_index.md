---
title: HtmlSaveOptions.ExportPageSetup
second_title: Aspose.Words for .NET API 参考
description: HtmlSaveOptions 财产. 指定页面设置是否导出为 HTMLMHTML 或 EPUB 默认为错误的.
type: docs
weight: 230
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

指定页面设置是否导出为 HTML、MHTML 或 EPUB。 默认为`错误的`.

```csharp
public bool ExportPageSetup { get; set; }
```

### 评论

每个[`Section`](../../../aspose.words/section/)在 Aspose.Words 文档模型中提供了页面设置信息 via[`PageSetup`](../../../aspose.words/pagesetup/)班级。当您将文档导出为 HTML 格式时，您可能需要保留此信息 以供进一步使用。特别是，页面设置对于渲染到分页媒体（打印） 或随后转换为本机 Microsoft Word 文件格式（DOCX、DOC、RTF、WML）可能很重要。

在大多数情况下，HTML 旨在用于在不执行分页的浏览器中查看。所以这个 feature 默认是不活动的。

### 例子

显示在保存为 HTML 时如何决定是否保留部分结构/页面设置信息。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TopMargin = 36.0;
pageSetup.BottomMargin = 36.0;
pageSetup.PaperSize = PaperSize.A5;

// 将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象
// 决定是保留还是放弃页面设置设置。
// 如果我们将“ExportPageSetup”标志设置为“true”，则输出 HTML 文档将包含我们的页面设置配置。
// 如果我们将“ExportPageSetup”标志设置为“false”，保存操作将丢弃我们的页面设置设置
// 对于第一部分，两个部分看起来相同。
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageSetup = exportPageSetup };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    Assert.True(outDocContents.Contains(
        "<style type=\"text/css\">" +
            "@page Section1 { size:419.55pt 595.3pt; margin:36pt 70.85pt }" +
            "@page Section2 { size:612pt 792pt; margin:70.85pt }" +
            "div.Section1 { page:Section1 }div.Section2 { page:Section2 }" +
        "</style>"));

    Assert.True(outDocContents.Contains(
        "<div class=\"Section1\">" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));

    Assert.True(outDocContents.Contains(
        "<div>" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlsaveoptions/)
* 部件 [Aspose.Words](../../../)


