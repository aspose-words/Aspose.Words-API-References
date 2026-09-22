---
title: "Aspose::Words::Document::StopTrackRevisions yöntemi"
linktitle: "StopTrackRevisions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::StopTrackRevisions yöntemi. Belge değişikliklerinin otomatik olarak revizyon olarak işaretlenmesini C++'ta durdurur."
type: docs
weight: 93000
url: /tr/cpp/aspose.words/document/stoptrackrevisions/
---
## Document::StopTrackRevisions method


Belge değişikliklerinin otomatik olarak revizyon olarak işaretlenmesini durdurur.

```cpp
void Aspose::Words::Document::StopTrackRevisions()
```


## Örnekler



Bir belgeyi düzenlerken revizyonları nasıl izleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir belgeyi düzenlemek genellikle revizyon sayılmaz, revizyon takibi başlatılana kadar.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Gelecek düzenlemelerin revizyon olarak sayılmaması için revizyon takibini durdurun.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Revizyonlar oluşturulduğunda onlara işlemin tarih ve saati atanır.
// Revizyonları izlemeye başladığımızda DateTime.MinValue geçirerek bunu devre dışı bırakabiliriz.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Bu revizyonları programlı olarak kabul/reddedebiliriz
// Document.AcceptAllRevisions gibi yöntemleri veya her revizyonun Accept yöntemini çağırarak.
// Microsoft Word'de, bunları "Review" -> "Changes" yoluyla manuel olarak işleyebiliriz.
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
