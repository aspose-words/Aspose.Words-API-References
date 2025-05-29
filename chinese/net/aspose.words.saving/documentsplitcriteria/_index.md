---
title: DocumentSplitCriteria Enum
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words.Saving.DocumentSplitCriteria 如何增强文档拆分功能，以实现最佳的 Html、Epub 和 Azw3 格式。简化您的保存流程！
type: docs
weight: 5710
url: /zh/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

指定保存文档时如何将其拆分为多个部分Html , Epub或者Azw3格式.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 文档未拆分。 |
| PageBreak | `1` | 文档在明确的分页符处被拆分成多个部分。 分页符可以通过[`PageBreak`](../../aspose.words/controlchar/pagebreak/)字符， 分节符指定新页面上新节的开始， 或具有其[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/)属性设置为`真的`. |
| ColumnBreak | `2` | 文档在分栏处被拆分成多个部分。 可以通过分栏指定[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/)字符或 分节符指定新列中新节的开始。 |
| SectionBreak | `4` | 文档在任何类型的分节符处被拆分为多个部分。 |
| HeadingParagraph | `8` | 文档按使用标题样式格式化的段落分成多个部分**标题 1**，**标题 2**等 一起使用[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/)指定要拆分的标题级别 （从 1 到指定级别）。 |

## 评论

`DocumentSplitCriteria`是一组可组合的标志。例如，您可以在同一个导出操作中，将 document 拆分为分页符和标题段落。

不同的标准可以部分重叠。例如，**标题 1**风格通常是 [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/)财产，因此它符合两个标准：PageBreak和 HeadingParagraph。一些分节符可能会导致分页符等。 在典型情况下，仅指定一个标志是最实用的选择。

## 例子

展示如何在将文档保存为 .epub 时使用特定编码。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 使用 SaveOptions 对象指定我们将保存的文档的编码。
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// 默认情况下，输出的 .epub 文档的所有内容都包含在一个 HTML 部分中。
// 拆分标准允许我们将文档分成几个 HTML 部分。
// 我们将设置标准将文档拆分为标题段落。
// 这对于无法读取大于特定大小的 HTML 文件的读者很有用。
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// 指定我们想要导出文档属性。
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
