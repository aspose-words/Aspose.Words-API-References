---
title: "Aspose::Words::Comment::get_Replies Methode"
linktitle: "get_Replies"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comment::get_Replies Methode. Gibt eine Sammlung von Comment-Objekten zurück, die unmittelbare Kinder des angegebenen Kommentars in C++ sind."
type: docs
weight: 12000
url: /de/cpp/aspose.words/comment/get_replies/
---
## Comment::get_Replies method


Gibt eine Sammlung von [Comment](../)-Objekten zurück, die unmittelbare Kinder des angegebenen Kommentars sind.

```cpp
System::SharedPtr<Aspose::Words::CommentCollection> Aspose::Words::Comment::get_Replies()
```


## Beispiele



Zeigt, wie man alle Kommentare eines Dokuments und deren Antworten ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// Hat ein Kommentar keinen Vorgänger, ist er ein „Top‑Level“-Kommentar im Gegensatz zu einem Antwort‑Kommentar.
// Gibt alle Top‑Level‑Kommentare zusammen mit allen möglichen Antworten aus.
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

## Siehe auch

* Class [CommentCollection](../../commentcollection/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
