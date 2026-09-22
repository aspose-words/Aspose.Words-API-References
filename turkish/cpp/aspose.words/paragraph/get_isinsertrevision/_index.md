---
title: "Aspose::Words::Paragraph::get_IsInsertRevision yöntemi"
linktitle: "get_IsInsertRevision"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::get_IsInsertRevision yöntemi. Değişiklik izleme etkinken bu nesne Microsoft Word'de eklenmişse Doğru döndürür; C++'da."
type: docs
weight: 14000
url: /tr/cpp/aspose.words/paragraph/get_isinsertrevision/
---
## Paragraph::get_IsInsertRevision method


Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür.

```cpp
bool Aspose::Words::Paragraph::get_IsInsertRevision()
```


## Örnekler



Revizyon paragraflarıyla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();
System::SharedPtr<Aspose::Words::Paragraph> para = body->get_FirstParagraph();

para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Paragraph 1. "));
body->AppendParagraph(u"Paragraph 2. ");
body->AppendParagraph(u"Paragraph 3. ");

// Yukarıdaki paragraflar revizyon değildir.
// Revizyon takibini başlattıktan sonra eklediğimiz paragraflar "Insert" revizyonları olarak kaydedilir.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

para = body->AppendParagraph(u"Paragraph 4. ");

ASSERT_TRUE(para->get_IsInsertRevision());

// Revizyon takibini başlattıktan sonra sildiğimiz paragraflar "Delete" revizyonları olarak kaydedilir.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = body->get_Paragraphs();

ASSERT_EQ(4, paragraphs->get_Count());

para = paragraphs->idx_get(2);
para->Remove();

// Bu paragraflar, silme revizyonunu kabul edene ya da reddedene kadar kalır.
// Revizyonu kabul etmek paragrafı kalıcı olarak kaldırır,
// ve revizyonu reddetmek, sanki hiç silinmemiş gibi belge içinde bırakır.
ASSERT_EQ(4, paragraphs->get_Count());
ASSERT_TRUE(para->get_IsDeleteRevision());

// Revizyonu kabul edin ve ardından paragrafın kaybolduğunu doğrulayın.
doc->AcceptAllRevisions();

ASSERT_EQ(3, paragraphs->get_Count());
ASSERT_EQ(0, para->get_Count());
ASSERT_EQ(System::String(u"Paragraph 1. \r") + u"Paragraph 2. \r" + u"Paragraph 4.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
