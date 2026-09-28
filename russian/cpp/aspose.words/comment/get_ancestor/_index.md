---
title: "Метод Aspose::Words::Comment::get_Ancestor"
linktitle: "get_Ancestor"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Comment::get_Ancestor. Возвращает объект родительского Comment. Возвращает **null** для комментариев верхнего уровня в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/comment/get_ancestor/
---
## Comment::get_Ancestor method


Возвращает объект родительского [Comment](../). Возвращает **null** для комментариев верхнего уровня.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::get_Ancestor()
```


## Примеры



Показывает, как вывести все комментарии документа и их ответы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// Если у комментария нет предка, он считается "верхнего уровня" комментарием, в отличие от комментария-ответа.
// Выведите все комментарии верхнего уровня вместе со всеми их ответами.
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

## См. также

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
