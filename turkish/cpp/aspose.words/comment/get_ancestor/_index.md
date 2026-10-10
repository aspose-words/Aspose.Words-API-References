---
title: "Aspose::Words::Comment::get_Ancestor metodu"
linktitle: "get_Ancestor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comment::get_Ancestor metodu. Üst Comment nesnesini döndürür. C++'da üst düzey yorumlar için null döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/comment/get_ancestor/
---
## Comment::get_Ancestor method


Üst [Comment](../) nesnesini döndürür. Üst düzey yorumlar için **null** döndürür.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::get_Ancestor()
```


## Örnekler



Bir belgenin tüm yorumlarını ve yanıtlarını nasıl yazdıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// Bir yorumun üst öğesi yoksa, yanıt türündeki bir yorumun aksine "top-level" bir yorumdur.
// Olabilecek tüm yanıtlarla birlikte tüm üst düzey yorumları yazdır.
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

## Ayrıca Bakınız

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
