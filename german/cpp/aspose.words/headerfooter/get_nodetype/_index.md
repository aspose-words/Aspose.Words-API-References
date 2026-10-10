---
title: "Aspose::Words::HeaderFooter::get_NodeType Methode"
linktitle: "get_NodeType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::HeaderFooter::get_NodeType Methode. Gibt HeaderFooter in C++ zurück."
type: docs
weight: 7000
url: /de/cpp/aspose.words/headerfooter/get_nodetype/
---
## HeaderFooter::get_NodeType method


Gibt [HeaderFooter](../../nodetype/) zurück.

```cpp
Aspose::Words::NodeType Aspose::Words::HeaderFooter::get_NodeType() const override
```


## Beispiele



Zeigt, wie man durch die Kinder eines zusammengesetzten Knotens iteriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// Ein Abschnitt ist ein zusammengesetzter Knoten und kann Kindknoten enthalten,
// aber nur, wenn diese Kindknoten vom Typ "Body" oder "HeaderFooter" sind.
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

## Siehe auch

* Enum [NodeType](../../nodetype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
