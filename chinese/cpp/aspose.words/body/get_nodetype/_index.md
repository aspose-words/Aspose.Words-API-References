---
title: "Aspose::Words::Body::get_NodeType 方法"
linktitle: "get_NodeType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Body::get_NodeType 方法。返回 Body（C++ 中）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/body/get_nodetype/
---
## Body::get_NodeType method


返回 [Body](../../nodetype/)。

```cpp
Aspose::Words::NodeType Aspose::Words::Body::get_NodeType() const override
```


## 示例



展示如何遍历复合节点的子节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// Section 是一种复合节点，可以包含子节点，
// 但仅当这些子节点的类型为 "Body" 或 "HeaderFooter"。
for (auto&& node : System::IterateOver(section))
{
    switch (node->get_NodeType())
    {
        case Aspose::Words::NodeType::Body:
            {
                auto body = System::ExplicitCast<Aspose::Words::Body>(node);

                std::cout << "Body:" << std::endl;
                std::cout << System::String::Format(u"\t\"{0}\"", body->GetText().Trim()) << std::endl;
                break;
            }

        case Aspose::Words::NodeType::HeaderFooter:
            {
                auto headerFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(node);

                std::cout << System::String::Format(u"HeaderFooter type: {0}:", headerFooter->get_HeaderFooterType()) << std::endl;
                std::cout << System::String::Format(u"\t\"{0}\"", headerFooter->GetText().Trim()) << std::endl;
                break;
            }

        default:
            {
                throw System::Exception(u"Unexpected node type in a section.");
            }

    }
}
```

## 另见

* Enum [NodeType](../../nodetype/)
* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
