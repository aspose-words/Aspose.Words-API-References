---
title: "Aspose::Words::IDocumentConverterPlugin::Convert 方法"
linktitle: "转换"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IDocumentConverterPlugin::Convert 方法。使用指定的输入输出流和保存选项在 C++ 中转换文档。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/idocumentconverterplugin/convert/
---
## IDocumentConverterPlugin::Convert method


使用指定的输入输出流和保存选项转换文档。

```cpp
virtual void Aspose::Words::IDocumentConverterPlugin::Convert(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<System::IO::Stream> outputStream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | 输入流。 |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | 文档加载选项。 |
| outputStream | System::SharedPtr\<System::IO::Stream\> | 输出流。 |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | 保存选项。 |

## 另见

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
