---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle 方法"
linktitle: "GetByTitle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle 方法。返回集合中具有指定标题的第一个结构化文档标签（C++）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection::GetByTitle method


返回集合中遇到的第一个具有指定标题的结构化文档标签。

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle(const System::String &title)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 标题 | const System::String\& | 结构化文档标签的标题。 |
## 备注


如果找不到具有指定标题的结构化文档标签，则返回 null。

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

* Interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
