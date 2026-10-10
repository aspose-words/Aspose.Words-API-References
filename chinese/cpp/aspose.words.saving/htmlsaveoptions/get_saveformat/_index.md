---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat method"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat method. 指定如果使用此保存选项对象，文档将以何种格式保存。可以是 Html、Mhtml、Epub、Azw3 或 Mobi（在 C++ 中）。"
type: docs
weight: 45000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_saveformat/
---
## HtmlSaveOptions::get_SaveFormat method


指定如果使用此保存选项对象，文档将以何种格式保存。可以是 [Html](../../../aspose.words/saveformat/)、[Mhtml](../../../aspose.words/saveformat/)、[Epub](../../../aspose.words/saveformat/)、[Azw3](../../../aspose.words/saveformat/) 或 [Mobi](../../../aspose.words/saveformat/)。

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
