---
title: "Aspose::Words::Comment::RemoveAllReplies 方法"
linktitle: "RemoveAllReplies"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comment::RemoveAllReplies 方法。删除 C++ 中对此评论的所有回复。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words/comment/removeallreplies/
---
## Comment::RemoveAllReplies method


移除此评论的所有回复。

```cpp
void Aspose::Words::Comment::RemoveAllReplies()
```


## 示例



展示如何删除评论回复。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"Another reply");

ASSERT_EQ(2, comment->get_Replies()->get_Count());

// 以下是删除评论回复的两种方法。
// 1 - 使用 "RemoveReply" 方法逐个删除评论的回复：
comment->RemoveReply(comment->get_Replies()->idx_get(0));

ASSERT_EQ(1, comment->get_Replies()->get_Count());

// 2 - 使用 "RemoveAllReplies" 方法一次性删除评论的所有回复：
comment->RemoveAllReplies();

ASSERT_EQ(0, comment->get_Replies()->get_Count());
```

## 另见

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
