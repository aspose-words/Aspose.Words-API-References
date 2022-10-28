---
title: RemoveReply
second_title: Aspose.Words for C++ API Reference
description: Removes the specified reply to this comment.
type: docs
weight: 170
url: /cpp/aspose.words/comment/removereply/
---
## Comment.RemoveReply method


Removes the specified reply to this comment.

```cpp
void Aspose::Words::Comment::RemoveReply(const System::SharedPtr<Aspose::Words::Comment> &reply)
```


| Parameter | Type | Description |
| --- | --- | --- |
| reply | const System::SharedPtr\<Aspose::Words::Comment\>\& | The comment node of the deleting reply. |

## Examples




Shows how to remove comment replies. 
```cpp
auto doc = MakeObject<Document>();

auto comment = MakeObject<Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(comment);

comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"Another reply");

ASSERT_EQ(2, comment->get_Replies()->LINQ_Count());

// Below are two ways of removing replies from a comment.
// 1 -  Use the "RemoveReply" method to remove replies from a comment individually:
comment->RemoveReply(comment->get_Replies()->idx_get(0));

ASSERT_EQ(1, comment->get_Replies()->LINQ_Count());

// 2 -  Use the "RemoveAllReplies" method to remove all replies from a comment at once:
comment->RemoveAllReplies();

ASSERT_EQ(0, comment->get_Replies()->LINQ_Count());
```

