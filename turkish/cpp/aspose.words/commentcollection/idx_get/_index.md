---
title: "Aspose::Words::CommentCollection::idx_get metodu"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CommentCollection::idx_get yöntemi. Verilen indeksteki bir Comment'u C++'ta alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/commentcollection/idx_get/
---
## CommentCollection::idx_get method


Verilen indeksteki bir [Comment](../../comment/) alır.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::CommentCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Koleksiyona bir indeks. |
## Açıklamalar


İndeks sıfır tabanlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi gösterir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

İndeks listedeki öğe sayısına eşit veya daha büyükse, bu null referans döndürür.

İndeks negatif ve mutlak değeri listedeki öğe sayısından büyükse, bu null referans döndürür.

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

* Class [Comment](../../comment/)
* Class [CommentCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
