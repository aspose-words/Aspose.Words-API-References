---
title: "Aspose::Words::Body::get_NodeType метод"
linktitle: "get_NodeType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Body::get_NodeType метод. Возвращает Body в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/body/get_nodetype/
---
## Body::get_NodeType method


Возвращает [Body](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::Body::get_NodeType() const override
```


## Примеры



Показывает, как перебрать дочерние элементы составного узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// Секция является составным узлом и может содержать дочерние узлы,
// но только если эти дочерние узлы имеют тип \"Body\" или \"HeaderFooter\".
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

## См. также

* Enum [NodeType](../../nodetype/)
* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
