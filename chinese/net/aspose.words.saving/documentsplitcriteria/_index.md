---
title: Enum DocumentSplitCriteria
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.DocumentSplitCriteria 枚举. 指定保存时文档如何分割成多个部分Html Epub或者Azw3格式.
type: docs
weight: 4960
url: /zh/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

指定保存时文档如何分割成多个部分Html, Epub或者Azw3格式.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 文档未拆分。 |
| PageBreak | `1` | 文档在显式分页符处分成多个部分。 分页符可以由[`PageBreak`](../../aspose.words/controlchar/pagebreak/)字符， 分节符，指定新页面上新节的开始， 或具有其[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/)属性设置为`真的`. |
| ColumnBreak | `2` | 文档在分栏符处分成多个部分。 分栏符可以由[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/)字符 or 分节符，指定新列中新节的开始。 |
| SectionBreak | `4` | 文档在任何类型的分节符处分为多个部分。 |
| HeadingParagraph | `8` | 文档在使用标题样式格式化的段落中分为多个部分 **标题 1**, **标题 2**等 与以下一起使用[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/)指定要拆分的标题级别 （从 1 到指定级别）。 |

### 评论

`DocumentSplitCriteria`是一组可以组合的标志。例如，您可以在同一导出操作中在分页符和标题段落处拆分 document 。

不同的标准可能部分重叠。例如， **标题 1**风格经常被给出 [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/)属性，因此它符合两个标准：PageBreak和 HeadingParagraph。有些分节符会导致分页等情况。 在典型情况下，仅指定一个标志是最实用的选择。

### 例子

演示将文档保存为 .epub 时如何使用特定编码。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 使用 SaveOptions 对象指定我们将保存的文档的编码。
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// 默认情况下，输出 .epub 文档的所有内容都位于一个 HTML 部分中。
// 分割标准允许我们将文档分割成几个 HTML 部分。
// 我们将设置将文档拆分为标题段落的标准。
// 这对于无法读取大于特定大小的 HTML 文件的读者很有用。
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// 指定我们要导出文档属性。
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)


