---
title: "Aspose::Words::Section::ClearHeadersFooters method"
linktitle: "ClearHeadersFooters"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Section::ClearHeadersFooters method. Bu bölümün başlık ve altbilgilerini C++'ta temizler."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/section/clearheadersfooters/
---
## Section::ClearHeadersFooters() method


Bu bölümün üstbilgi ve altbilgilerini temizler.

```cpp
void Aspose::Words::Section::ClearHeadersFooters()
```

## Açıklamalar


Tüm başlık ve altbilgilerin metni temizlenir, ancak [HeaderFooter](../../headerfooter/) nesneleri kendileri kaldırılmaz.

Bu, bu bölümün başlık ve altbilgilerini önceki bölümün başlık ve altbilgilerine bağlar.

## Örnekler



Bir bölümdeki tüm başlık ve altbilgilerin içeriğini temizlemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the primary header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the primary footer.");

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(u"This is the primary header.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"This is the primary footer.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// Bu bölümdeki tüm başlık ve altbilgileri tüm içeriklerinden boşaltın.
// Başlık ve altbilgiler hâlâ mevcut olacak ancak gösterilecek bir şey olmayacak.
doc->get_FirstSection()->ClearHeadersFooters();

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Section::ClearHeadersFooters(bool) method


Bu bölümün üstbilgi ve altbilgilerini temizler.

```cpp
void Aspose::Words::Section::ClearHeadersFooters(bool preserveWatermarks)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| preserveWatermarks | bool | Su işaretleri kaldırılmayacaksa doğru. |
## Açıklamalar


Tüm başlık ve altbilgilerin metni temizlenir, ancak [HeaderFooter](../../headerfooter/) nesneleri kendileri kaldırılmaz.

Bu, bu bölümün başlık ve altbilgilerini önceki bölümün başlık ve altbilgilerine bağlar.

## Örnekler



Başlık ve altbilginin içeriğini su işaretiyle ya da su işareti olmadan temizlemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Düz metin filigranı ekleyin.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Başlık ve altbilgilerin içeriğe sahip olduğundan emin olun.
System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"First header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"Second header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"Third header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"First footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"Second footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"Third footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// Su işaretleri dışındaki tüm başlık ve altbilgi içeriğini kaldırır.
doc->get_FirstSection()->ClearHeadersFooters(true);

headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
ASSERT_EQ(Aspose::Words::WatermarkType::Text, doc->get_Watermark()->get_Type());

// Su işaretleri dahil tüm başlık ve altbilgi içeriğini kaldırır.
doc->get_FirstSection()->ClearHeadersFooters(false);
ASSERT_EQ(Aspose::Words::WatermarkType::None, doc->get_Watermark()->get_Type());
```

## Ayrıca Bakınız

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
