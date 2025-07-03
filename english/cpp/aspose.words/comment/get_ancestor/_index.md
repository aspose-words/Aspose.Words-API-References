---
title: Aspose::Words::Comment::get_Ancestor method
linktitle: get_Ancestor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comment::get_Ancestor method. Returns the parent Comment object. Returns null for top-level comments in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/comment/get_ancestor/
---
## Comment::get_Ancestor method


Returns the parent [Comment](../) object. Returns **null** for top-level comments.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::get_Ancestor()
```


## Examples



Shows how to print all of a document's comments and their replies. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
// Print all top-level comments along with any replies they may have.
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

## See Also

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
