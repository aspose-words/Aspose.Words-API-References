---
title: "Aspose::Words::Saving::DocumentSplitCriteria enum"
linktitle: "DocumentSplitCriteria"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DocumentSplitCriteria enum. 指定在 C++ 中将文档保存为 Html、Epub 或 Azw3 格式时，文档如何拆分为多个部分。"
type: docs
weight: 52000
url: /zh/cpp/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enum


指定在将文档保存为 [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) 或 [Azw3](../../aspose.words/saveformat/) 格式时，文档如何拆分为多个部分。

```cpp
enum class DocumentSplitCriteria
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 文档未拆分。 |
| PageBreak | 1 | 文档在显式分页符处拆分为多个部分。分页符可以通过 [PageBreak](../../aspose.words/controlchar/pagebreak/) 字符、在新页面上开始新节的节分隔符，或其 [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) 属性设置为 **true** 的段落来指定。 |
| ColumnBreak | 2 | 文档在列分隔符处拆分为多个部分。列分隔符可以通过 [ColumnBreak](../../aspose.words/controlchar/columnbreak/) 字符或在新列中开始新节的节分隔符来指定。 |
| SectionBreak | 4 | 文档在任何类型的节分隔符处拆分为多个部分。 |
| HeadingParagraph | 8 | 文档在使用标题样式 **Heading 1**、**Heading 2** 等格式化的段落处拆分为多个部分。结合 [DocumentSplitHeadingLevel](../htmlsaveoptions/get_documentsplitheadinglevel/) 使用，以指定要拆分的标题级别（从 1 到指定的级别）。 |

## 备注


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

不同的条件可能部分重叠。例如，**Heading 1** 样式通常会设置 [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) 属性，因此它属于两种条件：[PageBreak](./) 和 [HeadingParagraph](./)。某些节分隔符可能会导致分页符，等等。通常情况下，仅指定一个标志是最实用的选择。

## 示例



展示如何在将文档保存为 .epub 时使用特定的编码。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 使用 SaveOptions 对象来指定我们将要保存的文档的编码。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// 默认情况下，输出的 .epub 文档的所有内容都位于一个 HTML 部分中。
// 拆分条件允许我们将文档划分为多个 HTML 部分。
// 我们将设置条件，以将文档拆分为标题段落。
// 这对于无法读取大于特定大小的 HTML 文件的阅读器很有用。
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// 指定我们要导出文档属性。
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
