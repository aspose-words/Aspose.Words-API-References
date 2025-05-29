---
title: ExportHeadersFootersMode Enum
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words ExportHeadersFootersMode 枚举，实现无缝 HTML、MHTML 或 EPUB 页眉和页脚导出。立即优化您的文档转换！
type: docs
weight: 5750
url: /zh/net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

指定如何将页眉和页脚导出为 HTML、MHTML 或 EPUB。

```csharp
public enum ExportHeadersFootersMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 页眉和页脚未导出。 |
| PerSection | `1` | 主页眉和页脚导出至每个部分的开头和结尾。 |
| FirstSectionHeaderLastSectionFooter | `2` | 第一部分的主页眉导出到文档的开头，主页脚导出到文档的结尾。 |
| FirstPageHeaderFooterPerSection | `3` | 第一页的页眉和页脚在每一节的开始和结束处导出。 |

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

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
