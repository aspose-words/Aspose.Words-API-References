---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title 方法"
linktitle: "get_Title"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title 方法。指定与此 SDT 关联的友好名称。在 C++ 中不能为空。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.markup/istructureddocumenttag/get_title/
---
## IStructuredDocumentTag::get_Title method


指定与此 **SDT** 关联的友好名称。不能为空。

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_Title() const =0
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
