---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen 方法"
linktitle: "get_KeepDocumentPartStreamOpen"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen 方法。指定在 C++ 中保存文档部件后，Aspose.Words 是否应保持流打开或将其关闭。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/documentpartsavingargs/get_keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen method


指定 Aspose.Words 在保存文档部分后是保持流打开还是关闭。

```cpp
bool Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen() const
```

## 备注


默认值为 **false**，Aspose.Words 在将文档部件写入后会关闭您在 [DocumentPartStream](../get_documentpartstream/) 属性中提供的流。指定 **true** 可保持流打开。请注意，即使在调用 [Save()](../) 或 [Save()](../) 时提供的主输出流，即使 [KeepDocumentPartStreamOpen](./) 设置为 **false**，Aspose.Words 也永远不会关闭该流。

## 另见

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
