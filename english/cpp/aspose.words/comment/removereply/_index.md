---
title: Aspose::Words::Comment::RemoveReply method
linktitle: RemoveReply
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comment::RemoveReply method. Removes the specified reply to this comment in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words/comment/removereply/
---
## Comment::RemoveReply method


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
auto doc = System::MakeObject<Aspose::Words::Document>();

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"Another reply");

ASSERT_EQ(2, comment->get_Replies()->get_Count());

// Below are two ways of removing replies from a comment.
// 1 -  Use the "RemoveReply" method to remove replies from a comment individually:
comment->RemoveReply(comment->get_Replies()->idx_get(0));

ASSERT_EQ(1, comment->get_Replies()->get_Count());

// 2 -  Use the "RemoveAllReplies" method to remove all replies from a comment at once:
comment->RemoveAllReplies();

ASSERT_EQ(0, comment->get_Replies()->get_Count());
```

## See Also

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
