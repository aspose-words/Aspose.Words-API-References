---
title: "Aspose::Words::Document::get_Revisions metodu"
linktitle: "get_Revisions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_Revisions metodu. Bu belgede mevcut olan revizyonların (izlenen değişiklikler) bir koleksiyonunu C++'ta alır."
type: docs
weight: 46000
url: /tr/cpp/aspose.words/document/get_revisions/
---
## Document::get_Revisions method


Bu belgede mevcut olan revizyonların (izlenen değişiklikler) koleksiyonunu alır.

```cpp
System::SharedPtr<Aspose::Words::RevisionCollection> Aspose::Words::Document::get_Revisions()
```

## Açıklamalar


Döndürülen koleksiyon bir "canlı" koleksiyondur, bu da belge içinde revizyon içeren bölümleri kaldırırsanız, silinen revizyonların bu koleksiyondan otomatik olarak kaybolacağı anlamına gelir.

## Örnekler



Bir belgede revizyonlarla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgenin normal düzenlenmesi bir revizyon olarak sayılmaz.
builder->Write(u"This does not count as a revision. ");

ASSERT_FALSE(doc->get_HasRevisions());

// Düzenlemelerimizi revizyon olarak kaydetmek için bir yazar tanımlamalı ve ardından izlemeye başlamalıyız.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

builder->Write(u"This is revision #1. ");

ASSERT_TRUE(doc->get_HasRevisions());
ASSERT_EQ(1, doc->get_Revisions()->get_Count());

// Bu bayrak, Microsoft Word'deki "Review" -> "Tracking" -> "Track Changes" seçeneğine karşılık gelir.
// "StartTrackRevisions" yöntemi değerini etkilemez,
// ve belge, değeri "false" olsa bile programlı olarak revizyonları izlemektedir.
// Bu belgeyi Microsoft Word ile açarsak, revizyonları izlemeyecek.
ASSERT_FALSE(doc->get_TrackRevisions());

// Belge oluşturucu ile metin ekledik, bu yüzden ilk revizyon bir ekleme türü revizyonudur.
System::SharedPtr<Aspose::Words::Revision> revision = doc->get_Revisions()->idx_get(0);
ASSERT_EQ(u"John Doe", revision->get_Author());
ASSERT_EQ(u"This is revision #1. ", revision->get_ParentNode()->GetText());
ASSERT_EQ(Aspose::Words::RevisionType::Insertion, revision->get_RevisionType());
ASSERT_EQ(revision->get_DateTime().get_Date(), System::DateTime::get_Now().get_Date());
ASPOSE_ASSERT_EQ(doc->get_Revisions()->get_Groups()->idx_get(0), revision->get_Group());

// Bir run kaldırarak silme türü revizyon oluşturun.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->Remove();

// Yeni bir revizyon eklemek, onu revizyon koleksiyonunun başına yerleştirir.
ASSERT_EQ(Aspose::Words::RevisionType::Deletion, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(2, doc->get_Revisions()->get_Count());

// Ekleme revizyonları, revizyonu kabul/reddetmeden önce bile belge gövdesinde görünür.
// Revizyonu reddetmek, düğümlerini gövdeden kaldırır. Aksine, silme revizyonlarını oluşturan düğümler
// revizyonu kabul edene kadar belgede kalır.
ASSERT_EQ(u"This does not count as a revision. This is revision #1.", doc->GetText().Trim());

// Silme revizyonunu kabul etmek, ebeveyn düğümünü paragraf metninden kaldırır
// ve ardından koleksiyonun revizyonunu kendisini kaldırır.
doc->get_Revisions()->idx_get(0)->Accept();

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1.", doc->GetText().Trim());

builder->Writeln(u"");
builder->Write(u"This is revision #2.");

// Şimdi düğümü taşıyarak hareketli bir revizyon türü oluşturun.
System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1);
System::SharedPtr<Aspose::Words::Node> endNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_NextSibling();
System::SharedPtr<Aspose::Words::Node> referenceNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0);

while (node != endNode)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = node->get_NextSibling();
    doc->get_FirstSection()->get_Body()->InsertBefore<System::SharedPtr<Aspose::Words::Node>>(node, referenceNode);
    node = nextNode;
}

ASSERT_EQ(Aspose::Words::RevisionType::Moving, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(8, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc->GetText().Trim());

// Hareketli revizyon artık indeks 1'de. İçeriğini atmak için revizyonu reddedin.
doc->get_Revisions()->idx_get(1)->Reject();

ASSERT_EQ(6, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1. \rThis is revision #2.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [RevisionCollection](../../revisioncollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
