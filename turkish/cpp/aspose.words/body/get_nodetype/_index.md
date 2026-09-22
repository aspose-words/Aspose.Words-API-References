---
title: "Aspose::Words::Body::get_NodeType yöntemi"
linktitle: "get_NodeType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Body::get_NodeType yöntemi. C++'da Body döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/body/get_nodetype/
---
## Body::get_NodeType method


Döndürür [Body](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::Body::get_NodeType() const override
```


## Örnekler



Bir birleşik düğümün alt öğeleri üzerinde yineleme yapmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// Bir Section, birleşik bir düğümdür ve alt düğümler içerebilir,
// ancak yalnızca bu alt düğümler "Body" veya "HeaderFooter" düğüm türünde ise.
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

## Ayrıca Bakınız

* Enum [NodeType](../../nodetype/)
* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
