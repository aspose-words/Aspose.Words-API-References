---
title: "Aspose::Words::Document::get_VersionsCount 方法"
linktitle: "get_VersionsCount"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_VersionsCount 方法。获取在 C++ 中存储于 DOC 文档的文档版本数量。"
type: docs
weight: 57000
url: /zh/cpp/aspose.words/document/get_versionscount/
---
## Document::get_VersionsCount method


获取存储在 DOC 文档中的文档版本数量。

```cpp
int32_t Aspose::Words::Document::get_VersionsCount()
```

## 备注


在 Microsoft Word 中，版本可通过 文件/版本 菜单访问。Microsoft Word 仅对 DOC 文件支持版本功能。

此属性可用于检测在使用 Aspose.Words 打开此文档之前，文档中是否存储了版本。Aspose.Words 不提供其他关于文档版本的支持。如果使用 Aspose.Words 保存此文档，文档将不带版本地保存。

## 示例



展示如何使用旧版 Microsoft Word 文档的版本计数功能。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Versions.doc");

// 我们可以读取文档的此属性，但在保存时无法保留它。
ASSERT_EQ(4, doc->get_VersionsCount());

doc->Save(get_ArtifactsDir() + u"Document.VersionsCount.doc");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.VersionsCount.doc");

ASSERT_EQ(0, doc->get_VersionsCount());
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
