---
title: "Aspose::Words::CompositeNode::GetEnumerator metod"
linktitle: "GetEnumerator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CompositeNode::GetEnumerator metod. Tillhandahåller stöd för iteration i foreach-stil över barnnoderna för detta objekt i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words/compositenode/getenumerator/
---
## CompositeNode::GetEnumerator method


Tillhandahåller stöd för foreach‑stiliteration över barnnoderna i den här noden.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Node>>> Aspose::Words::CompositeNode::GetEnumerator() override
```


## Exempel



Visar hur man skriver ut alla kommentarer i ett dokument och deras svar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// Om en kommentar saknar förfader är den en "top-level"-kommentar till skillnad från en svarskommentar.
// Skriv ut alla top-level-kommentarer tillsammans med eventuella svar de kan ha.
for (auto&& comment : comments->LINQ_OfType<System::SharedPtr<Aspose::Words::Comment> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Comment>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Comment> c)>>([](System::SharedPtr<Aspose::Words::Comment> c) -> bool
{
    return c->get_Ancestor() == nullptr;
})))->LINQ_ToList())
{
    std::cout << "Top-level comment:" << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\", by {1}", comment->GetText().Trim(), comment->get_Author()) << std::endl;
    std::cout << System::String::Format(u"Has {0} replies", comment->get_Replies()->get_Count()) << std::endl;
    for (auto&& commentReply : System::IterateOver<Aspose::Words::Comment>(comment->get_Replies()))
    {
        std::cout << System::String::Format(u"\t\"{0}\", by {1}", commentReply->GetText().Trim(), commentReply->get_Author()) << std::endl;
    }
    std::cout << std::endl;
}
```

## Se även

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
