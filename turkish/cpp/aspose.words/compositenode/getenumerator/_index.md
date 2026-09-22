---
title: "Aspose::Words::CompositeNode::GetEnumerator metodu"
linktitle: "GetEnumerator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CompositeNode::GetEnumerator metodu. C++'da bu düğümün çocuk düğümleri üzerinde foreach tarzı yinelemeyi destekler."
type: docs
weight: 11000
url: /tr/cpp/aspose.words/compositenode/getenumerator/
---
## CompositeNode::GetEnumerator method


Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Node>>> Aspose::Words::CompositeNode::GetEnumerator() override
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

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
