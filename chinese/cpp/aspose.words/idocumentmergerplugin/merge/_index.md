---
title: "Aspose::Words::IDocumentMergerPlugin::Merge 方法"
linktitle: "合并"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IDocumentMergerPlugin::Merge 方法。使用指定的输入和输出流在 C++ 中将给定的输入 PDF 文档合并为单个输出 PDF 文档。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/idocumentmergerplugin/merge/
---
## IDocumentMergerPlugin::Merge method


使用指定的输入和输出流将给定的输入 PDF 文档合并为单个输出 PDF 文档。

```cpp
virtual void Aspose::Words::IDocumentMergerPlugin::Merge(System::SharedPtr<System::IO::Stream> outputStream, System::ArrayPtr<System::SharedPtr<System::IO::Stream>> inputStreams, System::ArrayPtr<System::SharedPtr<Aspose::Words::Loading::LoadOptions>> loadOptions)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | System::SharedPtr\<System::IO::Stream\> | 输出流。 |
| inputStreams | System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\> | 输入流。 |
| loadOptions | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\> | 输入文件的加载选项。 |

## 另见

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Interface [IDocumentMergerPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
