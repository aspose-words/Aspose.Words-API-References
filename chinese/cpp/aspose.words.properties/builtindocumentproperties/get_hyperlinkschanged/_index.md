---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged method"
linktitle: "get_HyperlinksChanged"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged method. 指示文档中的超链接是否已更改，使用 C++。"
type: docs
weight: 13500
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkschanged/
---
## BuiltInDocumentProperties::get_HyperlinksChanged method


指示文档中的超链接是否已更改。

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged()
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
