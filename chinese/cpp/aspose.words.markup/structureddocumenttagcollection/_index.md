---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection 类"
linktitle: "StructuredDocumentTagCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection 类。一个 IStructuredDocumentTag 实例的集合，表示指定范围内的结构化文档标签。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class


一个集合，包含在指定范围内表示结构化文档标签的 [IStructuredDocumentTag](../istructureddocumenttag/) 实例。要了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。

```cpp
class StructuredDocumentTagCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Count](./get_count/)() | 返回集合中结构化文档标签的数量。 |
| [GetById](./getbyid/)(int32_t) | 按标识符返回结构化文档标签。 |
| [GetByTag](./getbytag/)(const System::String\&) | 返回集合中遇到的第一个具有指定标签的结构化文档标签。 |
| [GetByTitle](./getbytitle/)(const System::String\&) | 返回集合中遇到的第一个具有指定标题的结构化文档标签。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 返回指定索引处的结构化文档标签。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | 移除具有指定标识符的结构化文档标签。 |
| [RemoveAt](./removeat/)(int32_t) | 移除指定索引处的结构化文档标签。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
