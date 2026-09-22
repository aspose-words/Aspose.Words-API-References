---
title: "Aspose::Words::Document::StartTrackRevisions yöntemi"
linktitle: "StartTrackRevisions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::StartTrackRevisions yöntemi. C++'ta belgeye programlı olarak yaptığınız sonraki tüm değişiklikleri otomatik olarak revizyon değişiklikleri olarak işaretlemeye başlar."
type: docs
weight: 92000
url: /tr/cpp/aspose.words/document/starttrackrevisions/
---
## Document::StartTrackRevisions(const System::String\&) method


Belgeye programlı olarak yaptığınız tüm sonraki değişiklikleri otomatik olarak revizyon değişiklikleri olarak işaretlemeye başlar.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
## Açıklamalar


Bu yöntemi çağırırsanız ve ardından belgeyi programlı olarak değiştirirseniz, belgeyi kaydedin ve daha sonra belgeyi MS Word'de açarsanız, bu değişiklikleri revizyon olarak göreceksiniz.

Şu anda Aspose.Words yalnızca düğüm eklemeleri ve silmelerinin izlenmesini destekler. Biçimlendirme değişiklikleri revizyon olarak kaydedilmez.

Değişikliklerin otomatik izlenmesi, bu belgeyi düğüm manipülasyonlarıyla değiştirirken ve ayrıca [DocumentBuilder](../../documentbuilder/) kullanırken desteklenir.

Bu yöntem, [TrackRevisions](../get_trackrevisions/) seçeneğini değiştirmez ve revizyon takibi amacıyla değerini kullanmaz.

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
## Document::StartTrackRevisions(const System::String\&, System::DateTime) method


Belgeye programlı olarak yaptığınız tüm sonraki değişiklikleri otomatik olarak revizyon değişiklikleri olarak işaretlemeye başlar.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author, System::DateTime dateTime)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
## Açıklamalar


Bu yöntemi çağırırsanız ve ardından belgeyi programlı olarak değiştirirseniz, belgeyi kaydedin ve daha sonra belgeyi MS Word'de açarsanız, bu değişiklikleri revizyon olarak göreceksiniz.

Şu anda Aspose.Words yalnızca düğüm eklemeleri ve silmelerinin izlenmesini destekler. Biçimlendirme değişiklikleri revizyon olarak kaydedilmez.

Değişikliklerin otomatik izlenmesi, bu belgeyi düğüm manipülasyonlarıyla değiştirirken ve ayrıca [DocumentBuilder](../../documentbuilder/) kullanırken desteklenir.

Bu yöntem, [TrackRevisions](../get_trackrevisions/) seçeneğini değiştirmez ve revizyon takibi amacıyla değerini kullanmaz.

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
