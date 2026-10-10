---
title: "Aspose::Words::Body::get_NodeType metod"
linktitle: "get_NodeType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Body::get_NodeType metod. Returnerar Body i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/body/get_nodetype/
---
## Body::get_NodeType method


Returnerar [Body](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::Body::get_NodeType() const override
```


## Exempel



Visar hur man itererar genom barnen till en sammansatt nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// En sektion är en sammansatt nod och kan innehålla barnnoder,
// men endast om dessa barnnoder är av typen "Body" eller "HeaderFooter".
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

## Se även

* Enum [NodeType](../../nodetype/)
* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
