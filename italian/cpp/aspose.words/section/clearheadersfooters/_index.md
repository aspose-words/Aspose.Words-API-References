---
title: "Aspose::Words::Section::ClearHeadersFooters metodo"
linktitle: "ClearHeadersFooters"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Section::ClearHeadersFooters metodo. Cancella le intestazioni e i piè di pagina di questa sezione in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/section/clearheadersfooters/
---
## Section::ClearHeadersFooters() method


Cancella le intestazioni e i piè di pagina di questa sezione.

```cpp
void Aspose::Words::Section::ClearHeadersFooters()
```

## Note


Il testo di tutte le intestazioni e i piè di pagina viene cancellato, ma gli oggetti [HeaderFooter](../../headerfooter/) stessi non vengono rimossi.

Questo rende le intestazioni e i piè di pagina di questa sezione collegati a quelli della sezione precedente.

## Esempi



Mostra come cancellare il contenuto di tutte le intestazioni e i piè di pagina in una sezione.
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

// Svuota tutte le intestazioni e i piè di pagina di questa sezione da tutti i loro contenuti.
// Le intestazioni e i piè di pagina stessi saranno ancora presenti ma non avranno nulla da visualizzare.
doc->get_FirstSection()->ClearHeadersFooters();

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
```

## Vedi anche

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Section::ClearHeadersFooters(bool) method


Cancella le intestazioni e i piè di pagina di questa sezione.

```cpp
void Aspose::Words::Section::ClearHeadersFooters(bool preserveWatermarks)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| preserveWatermarks | bool | True se le filigrane non devono essere rimosse. |
## Note


Il testo di tutte le intestazioni e i piè di pagina viene cancellato, ma gli oggetti [HeaderFooter](../../headerfooter/) stessi non vengono rimossi.

Questo rende le intestazioni e i piè di pagina di questa sezione collegati a quelli della sezione precedente.

## Esempi



Mostra come cancellare il contenuto di intestazioni e piè di pagina con o senza una filigrana.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Aggiungi una filigrana di testo semplice.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Assicurati che le intestazioni e i piè di pagina contengano contenuto.
System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"First header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"Second header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"Third header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"First footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"Second footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"Third footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// Rimuove tutto il contenuto di intestazioni e piè di pagina eccetto le filigrane.
doc->get_FirstSection()->ClearHeadersFooters(true);

headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
ASSERT_EQ(Aspose::Words::WatermarkType::Text, doc->get_Watermark()->get_Type());

// Rimuove tutto il contenuto di intestazioni e piè di pagina incluse le filigrane.
doc->get_FirstSection()->ClearHeadersFooters(false);
ASSERT_EQ(Aspose::Words::WatermarkType::None, doc->get_Watermark()->get_Type());
```

## Vedi anche

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
