---
title: "Aspose::Words::HeaderFooter::get_NodeType método"
linktitle: "get_NodeType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::HeaderFooter::get_NodeType método. Devuelve HeaderFooter en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/headerfooter/get_nodetype/
---
## HeaderFooter::get_NodeType method


Devuelve [HeaderFooter](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::HeaderFooter::get_NodeType() const override
```


## Ejemplos



Muestra cómo iterar a través de los hijos de un nodo compuesto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// Una Section es un nodo compuesto y puede contener nodos hijos,
// pero solo si esos nodos hijos son de tipo nodo "Body" o "HeaderFooter".
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

## Ver también

* Enum [NodeType](../../nodetype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
