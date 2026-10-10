---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream 方法"
linktitle: "get_DocumentPartStream"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream 方法。允许在 C++ 中指定文档部件将被保存到的流。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartstream/
---
## DocumentPartSavingArgs::get_DocumentPartStream method


允许指定文档部件将保存到的流。

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream() const
```

## 备注


此属性允许您在 HTML 导出期间将文档部件保存到流而不是文件。

默认值为 **null**。当此属性为 **null** 时，文档部件将保存到在 [DocumentPartFileName](../get_documentpartfilename/) 属性中指定的文件。

当通过 [Save()](../) 或 [Save()](../) 请求以 HTML 格式保存到流，并且即将保存第一个文档部分时，Aspose.Words 在此建议使用调用方最初传入的主输出流。

当保存为基于 HTML 的容器格式 EPUB 时，不能指定 [DocumentPartStream](./)，因为所有子部分将被封装到单个输出包中。

## 另见

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
