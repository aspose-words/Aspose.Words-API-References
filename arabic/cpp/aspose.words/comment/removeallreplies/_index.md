---
title: "طريقة Aspose::Words::Comment::RemoveAllReplies"
linktitle: "RemoveAllReplies"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Comment::RemoveAllReplies. يزيل جميع الردود على هذا التعليق في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words/comment/removeallreplies/
---
## Comment::RemoveAllReplies method


يزيل جميع الردود على هذا التعليق.

```cpp
void Aspose::Words::Comment::RemoveAllReplies()
```


## أمثلة



يعرض كيفية إزالة ردود التعليق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"Another reply");

ASSERT_EQ(2, comment->get_Replies()->get_Count());

// فيما يلي طريقتان لإزالة الردود من التعليق.
// 1 -  استخدم طريقة \"RemoveReply\" لإزالة الردود من التعليق بشكل فردي:
comment->RemoveReply(comment->get_Replies()->idx_get(0));

ASSERT_EQ(1, comment->get_Replies()->get_Count());

// 2 -  استخدم طريقة \"RemoveAllReplies\" لإزالة جميع الردود من التعليق مرة واحدة:
comment->RemoveAllReplies();

ASSERT_EQ(0, comment->get_Replies()->get_Count());
```

## انظر أيضًا

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
