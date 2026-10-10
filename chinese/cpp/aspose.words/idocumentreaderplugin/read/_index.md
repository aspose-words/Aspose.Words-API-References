---
title: "Aspose::Words::IDocumentReaderPlugin::Read 方法"
linktitle: "读取"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IDocumentReaderPlugin::Read 方法。在 C++ 中将从指定流读取数据到 Document 实例中。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/idocumentreaderplugin/read/
---
## IDocumentReaderPlugin::Read method


将数据从指定流读取到 [Document](../../document/) 实例中。

```cpp
virtual void Aspose::Words::IDocumentReaderPlugin::Read(System::SharedPtr<System::IO::Stream> src, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Document> document)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| src | System::SharedPtr\<System::IO::Stream\> | 用于读取文档的源流。 |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | 用于加载文档的附加加载选项。 |
| document | System::SharedPtr\<Aspose::Words::Document\> | 用于读取数据的 [Document](../../document/) 类实例。如果该实例已包含一些内容，将被源流中的数据覆盖。 |

## 另见

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../../document/)
* Interface [IDocumentReaderPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
