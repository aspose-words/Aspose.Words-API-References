---
title: "Aspose::Words::Comment::get_Replies 方法"
linktitle: "get_Replies"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comment::get_Replies 方法。返回一个 Comment 对象的集合，这些对象是指定评论的直接子评论（C++）。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/comment/get_replies/
---
## Comment::get_Replies method


返回一个 [Comment](../) 对象的集合，这些对象是指定评论的直接子评论。

```cpp
System::SharedPtr<Aspose::Words::CommentCollection> Aspose::Words::Comment::get_Replies()
```


## 示例



展示如何打印文档的所有评论及其回复。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// 如果评论没有父级，则它是"顶层"评论，而不是回复类型的评论。
// 打印所有顶层评论以及它们可能拥有的任何回复。
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

## 另见

* Class [CommentCollection](../../commentcollection/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
