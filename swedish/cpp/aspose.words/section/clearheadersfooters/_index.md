---
title: "Aspose::Words::Section::ClearHeadersFooters‑metod"
linktitle: "ClearHeadersFooters"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Section::ClearHeadersFooters‑metod. Rensar sidhuvuden och sidfötter för denna sektion i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/section/clearheadersfooters/
---
## Section::ClearHeadersFooters() method


Rensar rubrikerna och sidfötterna i detta avsnitt.

```cpp
void Aspose::Words::Section::ClearHeadersFooters()
```

## Anmärkningar


Texten i alla sidhuvuden och sidfötter rensas, men [HeaderFooter](../../headerfooter/)-objekten själva tas inte bort.

Detta gör att sidhuvuden och sidfötter i denna sektion länkas till sidhuvuden och sidfötter i föregående sektion.

## Exempel



Visar hur man rensar innehållet i alla sidhuvuden och sidfötter i en sektion.
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

// Töm alla sidhuvuden och sidfötter i denna sektion på allt deras innehåll.
// Sidhuvuden och sidfötter kommer fortfarande att finnas kvar men har inget att visa.
doc->get_FirstSection()->ClearHeadersFooters();

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
```

## Se även

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Section::ClearHeadersFooters(bool) method


Rensar rubrikerna och sidfötterna i detta avsnitt.

```cpp
void Aspose::Words::Section::ClearHeadersFooters(bool preserveWatermarks)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| preserveWatermarks | bool | True om vattenstämplarna inte ska tas bort. |
## Anmärkningar


Texten i alla sidhuvuden och sidfötter rensas, men [HeaderFooter](../../headerfooter/)-objekten själva tas inte bort.

Detta gör att sidhuvuden och sidfötter i denna sektion länkas till sidhuvuden och sidfötter i föregående sektion.

## Exempel



Visar hur man rensar innehållet i sidhuvud och sidfot med eller utan en vattenstämpel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Lägg till ett vattenmärke i klartext.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Se till att sidhuvuden och sidfötter har innehåll.
System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"First header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"Second header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"Third header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"First footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"Second footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"Third footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// Tar bort allt innehåll i sidhuvud och sidfot förutom vattenstämplar.
doc->get_FirstSection()->ClearHeadersFooters(true);

headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
ASSERT_EQ(Aspose::Words::WatermarkType::Text, doc->get_Watermark()->get_Type());

// Tar bort allt innehåll i sidhuvud och sidfot inklusive vattenstämplar.
doc->get_FirstSection()->ClearHeadersFooters(false);
ASSERT_EQ(Aspose::Words::WatermarkType::None, doc->get_Watermark()->get_Type());
```

## Se även

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
