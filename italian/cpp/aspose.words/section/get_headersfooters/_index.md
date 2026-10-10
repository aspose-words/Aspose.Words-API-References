---
title: "Aspose::Words::Section::get_HeadersFooters metodo"
linktitle: "get_HeadersFooters"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Section::get_HeadersFooters metodo. Fornisce l'accesso ai nodi delle intestazioni e dei piè di pagina della sezione in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/section/get_headersfooters/
---
## Section::get_HeadersFooters method


Fornisce l'accesso ai nodi delle intestazioni e dei piè di pagina della sezione.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooterCollection> Aspose::Words::Section::get_HeadersFooters()
```


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

* Class [HeaderFooterCollection](../../headerfootercollection/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
