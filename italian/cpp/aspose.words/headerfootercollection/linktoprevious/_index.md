---
title: "Metodo Aspose::Words::HeaderFooterCollection::LinkToPrevious"
linktitle: "LinkToPrevious"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::HeaderFooterCollection::LinkToPrevious. Collega o scollega l'intestazione o il piè di pagina specificato all'intestazione o al piè di pagina corrispondente nella sezione precedente in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/headerfootercollection/linktoprevious/
---
## HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType, bool) method


Collega o scollega l'header o il footer specificato al corrispondente header o footer nella sezione precedente.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType headerFooterType, bool isLinkToPrevious)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Un valore [HeaderFooterType](../../headerfootertype/) che specifica l'intestazione o il piè di pagina da collegare/scollegare. |
| isLinkToPrevious | bool | **true** per collegare l'intestazione o il piè di pagina alla sezione precedente; **false** per scollegare. |
## Note


Se l'intestazione o il piè di pagina del tipo specificato non esiste, lo crea automaticamente.

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

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## HeaderFooterCollection::LinkToPrevious(bool) method


Collega o scollega tutti gli header e i footer ai corrispondenti header e footer nella sezione precedente.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(bool isLinkToPrevious)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| isLinkToPrevious | bool | **true** per collegare le intestazioni e i piè di pagina alla sezione precedente; **false** per scollegarle. |
## Note


Se una delle intestazioni o dei piè di pagina non esiste, li crea automaticamente.

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

* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
