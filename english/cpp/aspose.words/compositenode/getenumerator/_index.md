---
title: Aspose::Words::CompositeNode::GetEnumerator method
linktitle: GetEnumerator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::GetEnumerator method. Provides support for the for each style iteration over the child nodes of this node in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words/compositenode/getenumerator/
---
## CompositeNode::GetEnumerator method


Provides support for the for each style iteration over the child nodes of this node.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Node>>> Aspose::Words::CompositeNode::GetEnumerator() override
```


## Examples



Shows how to print all of a document's comments and their replies. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Comments.docx"));

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
// Print all top-level comments along with any replies they may have.
for (auto&& comment : comments->LINQ_OfType<System::SharedPtr<Aspose::Words::Comment>>()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Comment>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Comment> c)>>([](System::SharedPtr<Aspose::Words::Comment> c) -> bool
{
    return c->get_Ancestor() == nullptr;
})))->LINQ_ToList())
{
    System::Console::WriteLine(u"Top-level comment:");
    System::Console::WriteLine(System::String::Format(u"\t\"{0}\", by {1}", comment->GetText().Trim(), comment->get_Author()));
    System::Console::WriteLine(System::String::Format(u"Has {0} replies", comment->get_Replies()->get_Count()));
    for (auto&& commentReply : System::IterateOver<Aspose::Words::Comment>(comment->get_Replies()))
    {
        System::Console::WriteLine(System::String::Format(u"\t\"{0}\", by {1}", commentReply->GetText().Trim(), commentReply->get_Author()));
    }
    System::Console::WriteLine();
}
```

## See Also

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
