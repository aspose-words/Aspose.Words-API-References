---
title: "طريقة Aspose::Words::Comment::get_Author"
linktitle: "get_Author"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Comment::get_Author. يرجع أو يعيّن اسم المؤلف للتعليق في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/comment/get_author/
---
## Comment::get_Author method


يرجع أو يعيّن اسم المؤلف للتعليق.

```cpp
System::String Aspose::Words::Comment::get_Author() const
```

## ملاحظات


لا يمكن أن تكون **null**.

القيمة الافتراضية هي سلسلة فارغة.

## أمثلة



يوضح كيفية طباعة جميع تعليقات المستند وردودها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// إذا لم يكن للتعليق سلف، فهو تعليق "عالي المستوى" وليس تعليقًا من نوع الرد.
// اطبع جميع التعليقات عالية المستوى مع أي ردود قد تكون لها.
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

## انظر أيضًا

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
