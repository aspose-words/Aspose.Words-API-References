---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::Remove 方法"
linktitle: "Remove"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::Remove 方法。删除具有指定标识符的结构化文档标签（C++）。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection::Remove method


移除具有指定标识符的结构化文档标签。

```cpp
void Aspose::Words::Markup::StructuredDocumentTagCollection::Remove(int32_t id)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| id | int32_t | 结构化文档标签的标识符。 |

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

* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
