---
title: "Aspose::Words::Range::get_StructuredDocumentTags method"
linktitle: "get_StructuredDocumentTags"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Range::get_StructuredDocumentTags 方法。返回一个 StructuredDocumentTags 集合，表示范围内的所有结构化文档标签，在 C++ 中。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/range/get_structureddocumenttags/
---
## Range::get_StructuredDocumentTags method


返回一个 [StructuredDocumentTags](./) 集合，表示范围内的所有结构化文档标签。

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> Aspose::Words::Range::get_StructuredDocumentTags()
```


## 示例



展示如何删除结构化文档标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> structuredDocumentTags = doc->get_Range()->get_StructuredDocumentTags();
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt;
for (int32_t i = 0; i < structuredDocumentTags->get_Count(); i++)
{
    sdt = structuredDocumentTags->idx_get(i);
    std::cout << sdt->get_Title() << std::endl;
}

sdt = structuredDocumentTags->GetById(1691867797);
ASSERT_EQ(1691867797, sdt->get_Id());

ASSERT_EQ(5, structuredDocumentTags->get_Count());
// 按 Id 删除结构化文档标签。
structuredDocumentTags->Remove(1691867797);
// 删除位于位置 0 的结构化文档标签。
structuredDocumentTags->RemoveAt(0);
ASSERT_EQ(3, structuredDocumentTags->get_Count());
```

## 另见

* Class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
