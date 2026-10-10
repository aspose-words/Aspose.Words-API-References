---
title: "Aspose::Words::HeaderFooterCollection classe"
linktitle: "HeaderFooterCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::HeaderFooterCollection classe. Fornisce accesso tipizzato ai nodi HeaderFooter di una Section. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 32000
url: /it/cpp/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class


Fornisce accesso tipizzato ai nodi [HeaderFooter](../headerfooter/) di una [Section](../section/). Per saperne di più, visita l'articolo di documentazione [Working with Headers and Footers](https://docs.aspose.com/words/cpp/working-with-headers-and-footers/).

```cpp
class HeaderFooterCollection : public Aspose::Words::NodeCollection
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Aggiunge un nodo alla fine della collezione. |
| [Clear](../nodecollection/clear/)() | Rimuove tutti i nodi da questa collezione e dal documento. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determina se un nodo è nella collezione. |
| [get_Count](../nodecollection/get_count/)() | Ottiene il numero di nodi nella collezione. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Fornisce una semplice iterazione in stile "foreach" sulla collezione di nodi. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Recupera un [HeaderFooter](../headerfooter/) all'indice fornito. |
| [idx_get](./idx_get/)(Aspose::Words::HeaderFooterType) | Recupera un [HeaderFooter](../headerfooter/) del tipo specificato. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserisce un nodo nella collezione all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LinkToPrevious](./linktoprevious/)(bool) | Collega o scollega tutti gli header e i footer ai corrispondenti header e footer nella sezione precedente. |
| [LinkToPrevious](./linktoprevious/)(Aspose::Words::HeaderFooterType, bool) | Collega o scollega l'header o il footer specificato al corrispondente header o footer nella sezione precedente. |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](./toarray/)() | Copia tutti i **HeaderFooter** dalla raccolta in un nuovo array di **HeaderFooter**. |
| static [Type](./type/)() |  |
## Note


Può esserci al massimo uno [HeaderFooter](../headerfooter/)

di ciascun [HeaderFooterType](../headerfootertype/) per [Section](../section/).

[HeaderFooter](../headerfooter/) objects can occur in any order in the collection.

## Esempi



Mostra come creare un'intestazione e un piè di pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un'intestazione e aggiungi un paragrafo ad essa. Il testo in quel paragrafo
// apparirà nella parte superiore di ogni pagina di questa sezione, sopra il testo principale.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Crea un piè di pagina e aggiungi un paragrafo ad esso. Il testo in quel paragrafo
// apparirà nella parte inferiore di ogni pagina di questa sezione, sotto il testo principale.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```


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

## Vedi anche

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
