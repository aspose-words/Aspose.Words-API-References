---
title: "Aspose::Words::Comment::get_Replies metod"
linktitle: "get_Replies"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comment::get_Replies metod. Returnerar en samling av Comment‑objekt som är omedelbara barn till den angivna kommentaren i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words/comment/get_replies/
---
## Comment::get_Replies method


Returnerar en samling av [Comment](../)‑objekt som är omedelbara barn till den angivna kommentaren.

```cpp
System::SharedPtr<Aspose::Words::CommentCollection> Aspose::Words::Comment::get_Replies()
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

* Class [CommentCollection](../../commentcollection/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
