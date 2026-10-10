---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection 方法"
linktitle: "get_IsMultiSection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection 方法。如果此实例是范围（多节）结构化文档标签，则返回 true（在 C++ 中）。"
type: docs
weight: 3500
url: /zh/cpp/aspose.words.markup/istructureddocumenttag/get_ismultisection/
---
## IStructuredDocumentTag::get_IsMultiSection method


如果此实例是范围（多节）结构化文档标签，则返回 true。

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection()=0
```


## 示例



展示如何获取结构化文档标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// 按 Id 获取结构化文档标签。
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// 按 Title 获取结构化文档标签或范围标签。
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## 另见

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
