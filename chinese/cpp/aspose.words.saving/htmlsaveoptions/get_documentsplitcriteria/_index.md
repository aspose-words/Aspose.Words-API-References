---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria 方法"
linktitle: "get_DocumentSplitCriteria"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria 方法。指定在保存为 Html、Epub 或 Azw3 格式时文档应如何拆分。默认在 C++ 中 HTML 为 None，EPUB 和 AZW3 为 HeadingParagraph。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitcriteria/
---
## HtmlSaveOptions::get_DocumentSplitCriteria method


指定在保存为 [Html](../../../aspose.words/saveformat/)、[Epub](../../../aspose.words/saveformat/) 或 [Azw3](../../../aspose.words/saveformat/) 格式时文档应如何拆分。默认在 HTML 为 [None](../../documentsplitcriteria/)，在 EPUB 和 AZW3 为 [HeadingParagraph](../../documentsplitcriteria/)。

```cpp
Aspose::Words::Saving::DocumentSplitCriteria Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria() const
```

## 备注


通常，您希望文档保存为单个 HTML 文件。但在某些情况下，最好将输出拆分为多个较小的 HTML 页面。保存为 HTML 格式时，这些页面将输出到各个文件或流中。保存为 EPUB 格式时，它们将被合并到相应的包中。

在以 MHTML 格式保存时，文档无法拆分。

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

* Enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
