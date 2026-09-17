---
title: "Aspose::Words::Section::get_HeadersFooters méthode"
linktitle: "get_HeadersFooters"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Section::get_HeadersFooters méthode. Fournit l’accès aux nœuds des en-têtes et pieds de page de la section en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words/section/get_headersfooters/
---
## Section::get_HeadersFooters method


Fournit l'accès aux nœuds des en-têtes et pieds de page de la section.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooterCollection> Aspose::Words::Section::get_HeadersFooters()
```


## Exemples



Montre comment supprimer tous les pieds de page d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Parcourez chaque section et supprimez les pieds de page de tous types.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // Il existe trois types d'en-têtes et de pieds de page.
    // 1 -  Le "First" en-tête/pied de page, qui n'apparaît que sur la première page d'une section.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  Le "Primary" en-tête/pied de page, qui apparaît sur les pages impaires.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  Le "Even" en-tête/pied de page, qui apparaît sur les pages paires.
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


Montre comment remplacer du texte dans le pied de page d’un document.
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

## Voir aussi

* Class [HeaderFooterCollection](../../headerfootercollection/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
