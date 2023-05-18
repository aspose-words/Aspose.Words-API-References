---
title: Aspose::Words::HeaderFooter::get_NodeType method
linktitle: get_NodeType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::HeaderFooter::get_NodeType method. Returns HeaderFooter in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/headerfooter/get_nodetype/
---
## HeaderFooter::get_NodeType method


Returns [HeaderFooter](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::HeaderFooter::get_NodeType() const override
```


## Examples



Shows how to iterate through the children of a composite node. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

SharedPtr<Section> section = doc->get_FirstSection();

// A Section is a composite node and can contain child nodes,
// but only if those child nodes are of a "Body" or "HeaderFooter" node type.
for (const auto& node : System::IterateOver(section))
{
    switch (node->get_NodeType())
    {
    case NodeType::Body: {
        auto body = System::ExplicitCast<Body>(node);

        std::cout << "Body:" << std::endl;
        std::cout << "\t\"" << body->GetText().Trim() << "\"" << std::endl;
        break;
    }

    case NodeType::HeaderFooter: {
        auto headerFooter = System::ExplicitCast<HeaderFooter>(node);

        std::cout << String::Format(u"HeaderFooter type: {0}:", headerFooter->get_HeaderFooterType()) << std::endl;
        std::cout << "\t\"" << headerFooter->GetText().Trim() << "\"" << std::endl;
        break;
    }

    default: {
        throw System::Exception(u"Unexpected node type in a section.");
    }
    }
}
```

## See Also

* Enum [NodeType](../../nodetype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
