---
title: Aspose::Words::CommentCollection::idx_get method
linktitle: idx_get
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CommentCollection::idx_get method. Retrieves a Comment at the given index in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/commentcollection/idx_get/
---
## CommentCollection::idx_get method


Retrieves a [Comment](../../comment/) at the given index.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::CommentCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the collection. |
## Remarks


The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

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

## See Also

* Class [Comment](../../comment/)
* Class [CommentCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
