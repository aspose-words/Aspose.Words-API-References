---
title: "Aspose::Words::Document::RemoveExternalSchemaReferences 方法"
linktitle: "RemoveExternalSchemaReferences"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::RemoveExternalSchemaReferences 方法。删除此文档中 C++ 的外部 XML 架构引用。"
type: docs
weight: 68000
url: /zh/cpp/aspose.words/document/removeexternalschemareferences/
---
## Document::RemoveExternalSchemaReferences method


从此文档中删除外部 XML 架构引用。

```cpp
void Aspose::Words::Document::RemoveExternalSchemaReferences()
```


## 示例



展示如何从文档中删除所有外部 XML 架构引用。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"External XML schema.docx");

doc->RemoveExternalSchemaReferences();
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
