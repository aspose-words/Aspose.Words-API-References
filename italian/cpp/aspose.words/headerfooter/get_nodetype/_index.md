---
title: "Aspose::Words::HeaderFooter::get_NodeType metodo"
linktitle: "get_NodeType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::HeaderFooter::get_NodeType metodo. Restituisce HeaderFooter in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/headerfooter/get_nodetype/
---
## HeaderFooter::get_NodeType method


Restituisce [HeaderFooter](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::HeaderFooter::get_NodeType() const override
```


## Esempi



Mostra come iterare tra i figli di un nodo composito.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// Una Section è un nodo composito e può contenere nodi figlio,
// ma solo se quei nodi figlio sono di tipo "Body" o "HeaderFooter".
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

## Vedi anche

* Enum [NodeType](../../nodetype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
