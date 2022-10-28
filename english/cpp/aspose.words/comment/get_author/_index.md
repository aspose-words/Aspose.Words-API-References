---
title: get_Author
second_title: Aspose.Words for C++ API Reference
description: Returns or sets the author name for a comment.
type: docs
weight: 53
url: /cpp/aspose.words/comment/get_author/
---
## Comment.get_Author method


Returns or sets the author name for a comment.

```cpp
System::String Aspose::Words::Comment::get_Author() const
```


Cannot be null.

Default is empty string.

## Examples




Shows how to print all of a document's comments and their replies. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Comments.docx");

SharedPtr<NodeCollection> comments = doc->GetChildNodes(NodeType::Comment, true);

// If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
// Print all top-level comments along with any replies they may have.
auto hasNullAncestor = [](SharedPtr<Comment> c)
{
    return c->get_Ancestor() == nullptr;
};

for (auto comment : System::IterateOver(comments->LINQ_OfType<SharedPtr<Comment>>()->LINQ_Where(hasNullAncestor)))
{
    std::cout << "Top-level comment:" << std::endl;
    std::cout << "\t\"" << comment->GetText().Trim() << "\", by " << comment->get_Author() << std::endl;
    std::cout << "Has " << comment->get_Replies()->get_Count() << " replies" << std::endl;
    for (const auto& commentReply : System::IterateOver<Comment>(comment->get_Replies()))
    {
        std::cout << "\t\"" << commentReply->GetText().Trim() << "\", by " << commentReply->get_Author() << std::endl;
    }
    std::cout << std::endl;
}
```

