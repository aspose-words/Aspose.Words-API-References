---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop 方法"
linktitle: "get_ScaleCrop"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop 方法。指示文档缩略图是被裁剪还是按比例缩放以适应显示（C++）。"
type: docs
weight: 24500
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_scalecrop/
---
## BuiltInDocumentProperties::get_ScaleCrop method


指示文档缩略图是被裁剪还是按比例缩放以适应显示。

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop()
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
