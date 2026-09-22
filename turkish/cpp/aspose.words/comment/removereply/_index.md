---
title: "Aspose::Words::Comment::RemoveReply yöntemi"
linktitle: "RemoveReply"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comment::RemoveReply yöntemi. Bu, C++'ta bu yoruma verilen belirtilen yanıtı kaldırır."
type: docs
weight: 17000
url: /tr/cpp/aspose.words/comment/removereply/
---
## Comment::RemoveReply method


Bu yorum için belirtilen yanıtı kaldırır.

```cpp
void Aspose::Words::Comment::RemoveReply(const System::SharedPtr<Aspose::Words::Comment> &reply)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| yanıt | const System::SharedPtr\<Aspose::Words::Comment\>\& | Silinen yanıtın yorum düğümü. |

## Örnekler



Yorum yanıtlarını nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"Another reply");

ASSERT_EQ(2, comment->get_Replies()->get_Count());

// Aşağıda bir yorumdan yanıtları kaldırmanın iki yolu verilmiştir.
// 1 -  \"RemoveReply\" yöntemini kullanarak bir yorumdan yanıtları tek tek kaldırın:
comment->RemoveReply(comment->get_Replies()->idx_get(0));

ASSERT_EQ(1, comment->get_Replies()->get_Count());

// 2 -  \"RemoveAllReplies\" yöntemini kullanarak bir yorumdan tüm yanıtları bir anda kaldırın:
comment->RemoveAllReplies();

ASSERT_EQ(0, comment->get_Replies()->get_Count());
```

## Ayrıca Bakınız

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
