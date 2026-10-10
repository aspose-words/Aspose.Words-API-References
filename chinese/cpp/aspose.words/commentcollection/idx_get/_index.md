---
title: "Aspose::Words::CommentCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CommentCollection::idx_get 方法。检索在 C++ 中给定索引处的 Comment。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/commentcollection/idx_get/
---
## CommentCollection::idx_get method


检索给定索引处的 [Comment](../../comment/)。

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::CommentCollection::idx_get(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 集合中的索引。 |
## 备注


索引从零开始。

允许使用负索引，并表示从集合的末尾访问。例如 -1 表示最后一个项目，-2 表示倒数第二个，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负且其绝对值大于列表中的项目数，则返回空引用。

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

* Class [Comment](../../comment/)
* Class [CommentCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
