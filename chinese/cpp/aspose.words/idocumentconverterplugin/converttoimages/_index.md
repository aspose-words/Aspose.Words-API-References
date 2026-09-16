---
title: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages 方法"
linktitle: "转换为图像"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages 方法。将文档的页面从输入流转换为 C++ 中的图像数组。"
type: docs
weight: 2500
url: /zh/cpp/aspose.words/idocumentconverterplugin/converttoimages/
---
## IDocumentConverterPlugin::ConvertToImages method


将文档的页面从输入流转换为图像数组。

```cpp
virtual System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::IDocumentConverterPlugin::ConvertToImages(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | 输入流。 |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | 文档加载选项。 |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | 保存选项。 |

### ReturnValue

页面图像流数组。

## 另见

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
