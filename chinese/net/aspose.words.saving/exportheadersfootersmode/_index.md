---
title: Enum ExportHeadersFootersMode
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.ExportHeadersFootersMode 枚举. 指定如何将页眉和页脚导出为 HTMLMHTML 或 EPUB
type: docs
weight: 5000
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
| PerSection | `1` | 主页眉和页脚在每个部分的开头和结尾处导出。 |
| FirstSectionHeaderLastSectionFooter | `2` | 第一部分的主页眉在文档的开头导出，主页脚在末尾。 |
| FirstPageHeaderFooterPerSection | `3` | 在每个部分的开头和结尾处导出首页页眉和页脚。 |

### 例子

演示将文档保存为 HTML 时如何省略页眉/页脚。

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// 该文档包含页眉和页脚。我们可以通过“HeadersFooters”集合访问它们。
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// .html 等格式不会将文档拆分为多个页面，因此页眉/页脚的功能不会相同
// 当我们使用 Microsoft Word 打开 .docx 格式的文档时，就会出现这种情况。
// 如果我们将带有页眉/页脚的文档转换为 html，则转换会将页眉/页脚同化为正文。
// 我们可以使用 SaveOptions 对象在转换为 html 时省略页眉/页脚。
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// 打开我们保存的文档并验证它不包含标题文本
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### 也可以看看

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)


