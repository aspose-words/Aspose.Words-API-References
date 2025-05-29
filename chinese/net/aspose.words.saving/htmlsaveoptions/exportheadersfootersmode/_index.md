---
title: HtmlSaveOptions.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words for .NET
description: 了解 HtmlSaveOptions ExportHeadersFootersMode 属性如何优化 HTML、MHTML 和 EPUB 格式的页眉和页脚输出。最大化您的文档呈现效果！
type: docs
weight: 160
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

指定如何将页眉和页脚输出为 HTML、MHTML 或 EPUB。 默认值为PerSection对于 HTML/MHTML 和None适用于 EPUB。

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## 评论

由于 HTML 没有分页，因此很难将页眉和页脚有意义地输出为 HTML。

当此属性PerSection, Aspose.Words exports 仅在每个部分的开头和结尾处显示主页眉和页脚。

当FirstSectionHeaderLastSectionFooter 仅导出第一个主页眉和最后一个主页脚（包括链接到前一个）。

您可以通过将此属性 设置为None。

## 例子

展示如何在将文档保存为 HTML 时省略页眉/页脚。

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// 本文档包含页眉和页脚。我们可以通过“HeadersFooters”集合访问它们。
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// .html 等格式不会将文档拆分成页面，因此页眉/页脚的功能将有所不同
// 当我们使用 Microsoft Word 将文档以 .docx 格式打开时，它们就会发生。
// 如果我们将带有页眉/页脚的文档转换为 html，则转换将把页眉/页脚同化为正文。
// 我们可以使用 SaveOptions 对象在转换为 html 时省略页眉/页脚。
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// 打开我们保存的文档并验证它不包含标题的文本
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### 也可以看看

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
