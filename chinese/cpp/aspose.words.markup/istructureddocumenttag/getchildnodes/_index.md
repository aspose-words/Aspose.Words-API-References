---
title: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes 方法"
linktitle: "GetChildNodes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes 方法。返回在 C++ 中匹配指定类型的子节点的实时集合。"
type: docs
weight: 14500
url: /zh/cpp/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag::GetChildNodes method


返回一个实时集合，包含匹配指定类型的子节点。

```cpp
virtual System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)=0
```


## 示例



展示如何删除结构化文档标签，但保留内部内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// 此集合提供统一接口，用于访问有范围和无范围的结构化标签。
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// 在此我们可以通过有范围和无范围结构化标签的通用接口获取子节点。
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## 另见

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
