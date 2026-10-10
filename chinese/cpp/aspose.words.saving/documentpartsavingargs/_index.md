---
title: "Aspose::Words::Saving::DocumentPartSavingArgs class"
linktitle: "DocumentPartSavingArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DocumentPartSavingArgs 类。提供用于 DocumentPartSaving() 回调的数据。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class


提供用于 [DocumentPartSaving()](../idocumentpartsavingcallback/documentpartsaving/) 回调的数据。要了解更多信息，请访问 [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) 文档文章。

```cpp
class DocumentPartSavingArgs : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Document](./get_document/)() const | 获取正在保存的文档对象。 |
| [get_DocumentPartFileName](./get_documentpartfilename/)() const | 获取或设置文档部件将保存到的文件名（不含路径）。 |
| [get_DocumentPartStream](./get_documentpartstream/)() const | 允许指定文档部件将保存到的流。 |
| [get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/)() const | 指定 Aspose.Words 在保存文档部分后是保持流打开还是关闭。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DocumentPartFileName](./set_documentpartfilename/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName](./get_documentpartfilename/) 的 setter。 |
| [set_DocumentPartStream](./set_documentpartstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | 用于设置 [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream](./get_documentpartstream/) 的 setter。 |
| [set_DocumentPartStream](./set_documentpartstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepDocumentPartStreamOpen](./set_keepdocumentpartstreamopen/)(bool) | 用于设置 [Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


当 Aspose.Words 将文档保存为 HTML 或相关格式并指定了 [DocumentSplitCriteria](../htmlsaveoptions/get_documentsplitcriteria/) 时，文档会被拆分为多个部分，默认情况下，每个文档部分会保存到单独的文件中。

类 [DocumentPartSavingArgs](./) 允许您控制每个文档部分的保存方式。它可以重新定义文件名的生成方式，或通过提供您自己的流对象完全避免将文档部分保存为文件。

要将文档部分保存到流而不是文件，请使用 [DocumentPartStream](./get_documentpartstream/) 属性。
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
