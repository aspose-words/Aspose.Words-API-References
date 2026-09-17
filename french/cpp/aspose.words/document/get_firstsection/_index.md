---
title: "Aspose::Words::Document::get_FirstSection méthode"
linktitle: "get_FirstSection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_FirstSection méthode. Obtient la première section du document en C++."
type: docs
weight: 24000
url: /fr/cpp/aspose.words/document/get_firstsection/
---
## Document::get_FirstSection method


Obtient la première section du document.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_FirstSection()
```


## Exemples



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


Montre comment créer une nouvelle section avec un constructeur de document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un document vierge contient une section par défaut,
// qui contient des nœuds enfants que nous pouvons modifier.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Utilisez un constructeur de document pour ajouter du texte à la première section.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Créez une deuxième section en insérant un saut de section.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Chaque section possède ses propres paramètres de mise en page.
// Nous pouvons diviser le texte de la deuxième section en deux colonnes.
// Cela n'affectera pas le texte de la première section.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```


Montre comment itérer à travers les enfants d'un nœud composite.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// Une Section est un nœud composite et peut contenir des nœuds enfants,
// mais uniquement si ces nœuds enfants sont de type "Body" ou "HeaderFooter".
for (auto&& node : System::IterateOver(section))
{
    switch (node->get_NodeType())
    {
        case Aspose::Words::NodeType::Body:
            {
                auto body = System::ExplicitCast<Aspose::Words::Body>(node);

                std::cout << "Body:" << std::endl;
                std::cout << System::String::Format(u"\t\"{0}\"", body->GetText().Trim()) << std::endl;
                break;
            }

        case Aspose::Words::NodeType::HeaderFooter:
            {
                auto headerFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(node);

                std::cout << System::String::Format(u"HeaderFooter type: {0}:", headerFooter->get_HeaderFooterType()) << std::endl;
                std::cout << System::String::Format(u"\t\"{0}\"", headerFooter->GetText().Trim()) << std::endl;
                break;
            }

        default:
            {
                throw System::Exception(u"Unexpected node type in a section.");
            }

    }
}
```

## Voir aussi

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
