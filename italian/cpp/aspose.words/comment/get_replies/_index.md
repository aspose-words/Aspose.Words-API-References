---
title: "Metodo Aspose::Words::Comment::get_Replies"
linktitle: "get_Replies"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Comment::get_Replies. Restituisce una raccolta di oggetti Comment che sono figli immediati del commento specificato in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/comment/get_replies/
---
## Comment::get_Replies method


Restituisce una raccolta di oggetti [Comment](../) che sono figli immediati del commento specificato.

```cpp
System::SharedPtr<Aspose::Words::CommentCollection> Aspose::Words::Comment::get_Replies()
```


## Esempi



Mostra come stampare tutti i commenti di un documento e le loro risposte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// Se un commento non ha antenati, è un commento di "livello superiore" rispetto a un commento di tipo risposta.
// Stampa tutti i commenti di livello superiore insieme a eventuali risposte associate.
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

## Vedi anche

* Class [CommentCollection](../../commentcollection/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
