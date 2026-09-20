---
title: "Метод Aspose::Words::Comment::RemoveAllReplies"
linktitle: "RemoveAllReplies"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Comment::RemoveAllReplies. Удаляет все ответы к этому комментарию в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words/comment/removeallreplies/
---
## Comment::RemoveAllReplies method


Удаляет все ответы на этот комментарий.

```cpp
void Aspose::Words::Comment::RemoveAllReplies()
```


## Примеры



Показывает, как удалить ответы к комментариям.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"Another reply");

ASSERT_EQ(2, comment->get_Replies()->get_Count());

// Ниже представлены два способа удаления ответов из комментария.
// 1 -  Используйте метод \"RemoveReply\" для индивидуального удаления ответов из комментария:
comment->RemoveReply(comment->get_Replies()->idx_get(0));

ASSERT_EQ(1, comment->get_Replies()->get_Count());

// 2 -  Используйте метод \"RemoveAllReplies\" для одновременного удаления всех ответов из комментария:
comment->RemoveAllReplies();

ASSERT_EQ(0, comment->get_Replies()->get_Count());
```

## См. также

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
