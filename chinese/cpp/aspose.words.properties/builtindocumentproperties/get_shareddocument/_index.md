---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument 方法"
linktitle: "get_SharedDocument"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument 方法。指示文档在 C++ 中是否为共享文档。"
type: docs
weight: 25500
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_shareddocument/
---
## BuiltInDocumentProperties::get_SharedDocument method


指示文档是否为共享文档。

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument()
```

## 备注


Aspose.Words 不会更新此属性。

## 示例



展示如何获取扩展属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Extended properties.docx");
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_ScaleCrop());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_SharedDocument());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_HyperlinksChanged());
```

## 另见

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
