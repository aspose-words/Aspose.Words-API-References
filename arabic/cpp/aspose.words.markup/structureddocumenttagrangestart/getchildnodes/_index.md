---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes طريقة"
linktitle: "GetChildNodes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes طريقة. تُرجع مجموعة حية من عقد الأطفال التي تطابق الأنواع المحددة في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words.markup/structureddocumenttagrangestart/getchildnodes/
---
## StructuredDocumentTagRangeStart::GetChildNodes method


يرجع مجموعة حية من العقد الفرعية التي تطابق الأنواع المحددة.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTagRangeStart::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


## أمثلة



يظهر كيفية الحصول على عقد الأطفال من [StructuredDocumentTagRangeStart](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Child nodes count: {0}\n", tag->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count()) << std::endl;

for (auto&& node : System::IterateOver(tag->GetChildNodes(Aspose::Words::NodeType::Any, false)))
{
    std::cout << System::String::Format(u"\t|Child node type: {0}", node->get_NodeType()) << std::endl;
}

for (auto&& node : System::IterateOver(tag->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    std::cout << System::String::Format(u"\t|Child node text: {0}", node->GetText()) << std::endl;
}
```

## انظر أيضًا

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
