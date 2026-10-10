---
title: "Aspose::Words::HeaderFooterCollection::idx_get metodo"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::HeaderFooterCollection::idx_get metodo. Recupera un HeaderFooter del tipo specificato in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/headerfootercollection/idx_get/
---
## HeaderFooterCollection::idx_get(Aspose::Words::HeaderFooterType) method


Recupera un [HeaderFooter](../../headerfooter/) del tipo specificato.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooter> Aspose::Words::HeaderFooterCollection::idx_get(Aspose::Words::HeaderFooterType headerFooterType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Un valore [HeaderFooterType](../../headerfootertype/) che specifica il tipo di intestazione/piè di pagina da recuperare. |

## Esempi



Mostra come eliminare tutti i piè di pagina da un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Itera attraverso ogni sezione e rimuove i piè di pagina di ogni tipo.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // Esistono tre tipi di intestazioni e piè di pagina.
    // 1 -  L'intestazione/piè di pagina "First", che appare solo nella prima pagina di una sezione.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  L'intestazione/piè di pagina "Primary", che appare nelle pagine dispari.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  L'intestazione/piè di pagina "Even", che appare nelle pagine pari.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression3 = footer;
    if (condExpression3 != nullptr)
    {
        condExpression3->Remove();
    }

    ASSERT_EQ(0, section->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
    {
        return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsHeader();
    }))));
}

doc->Save(get_ArtifactsDir() + u"HeaderFooter.RemoveFooters.docx");
```


Mostra come sostituire il testo nel piè di pagina di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```

## Vedi anche

* Class [HeaderFooter](../../headerfooter/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## HeaderFooterCollection::idx_get(int32_t) method


Recupera un [HeaderFooter](../../headerfooter/) all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooter> Aspose::Words::HeaderFooterCollection::idx_get(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Un indice nella collezione. |
## Note


L'indice parte da zero.

Gli indici negativi sono consentiti e indicano l'accesso dalla fine della collezione. Per esempio, -1 indica l'ultimo elemento, -2 il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nella lista, questo restituisce un riferimento nullo.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nella lista, questo restituisce un riferimento nullo.

## Esempi



Mostra come collegare intestazioni e piè di pagina tra le sezioni.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// Passa alla prima sezione e crea un'intestazione e un piè di pagina. Per impostazione predefinita,
// l'intestazione e il piè di pagina appariranno solo nelle pagine della sezione che li contiene.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Possiamo collegare le intestazioni/piè di pagina di una sezione a quelle della sezione precedente
// per consentire alla sezione collegata di visualizzare le intestazioni/piè di pagina della sezione collegata.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Ogni sezione avrà comunque i propri oggetti intestazione/piè di pagina. Quando colleghiamo le sezioni,
// la sezione collegata visualizzerà le intestazioni/piè di pagina della sezione collegata mantenendo le proprie.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Collega le intestazioni/piè di pagina della terza sezione a quelle della seconda sezione.
// La seconda sezione è già collegata alle intestazioni/piè di pagina della prima sezione,
// quindi collegare alla seconda sezione creerà una catena di collegamenti.
// Le sezioni prima, seconda e ora la terza visualizzeranno tutte le intestazioni della prima sezione.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// Possiamo scollegare le intestazioni/piè di pagina di una sezione precedente passando "false" quando si chiama il metodo LinkToPrevious.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// Possiamo anche selezionare solo un tipo specifico di intestazione/piè di pagina da collegare usando questo metodo.
// La terza sezione ora avrà lo stesso piè di pagina delle seconde e prima sezioni, ma non l'intestazione.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Le intestazioni/piè di pagina della prima sezione non possono collegarsi a nulla perché non esiste una sezione precedente.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Tutte le intestazioni/piè di pagina della seconda sezione sono collegate alle intestazioni/piè di pagina della prima sezione.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Nella terza sezione, solo il piè di pagina è collegato al piè di pagina della prima sezione tramite la seconda sezione.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## Vedi anche

* Class [HeaderFooter](../../headerfooter/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
