---
title: "Énumération Aspose::Words::Loading::TxtTrailingSpacesOptions"
linktitle: "TxtTrailingSpacesOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::Loading::TxtTrailingSpacesOptions. Spécifie les options disponibles pour la gestion des espaces de fin lors de l'importation depuis un fichier texte en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.loading/txttrailingspacesoptions/
---
## TxtTrailingSpacesOptions enum


Spécifie les options disponibles pour la gestion des espaces de fin lors de l'importation depuis un fichier [Texte](../../aspose.words/loadformat/).

```cpp
enum class TxtTrailingSpacesOptions
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Rogner | 0 | Les espaces de fin sont rognés. |
| Conserver | 1 | Les espaces de fin sont conservés. |


## Exemples



Montre comment rogner les espaces blancs lors du chargement de documents texte brut.
```cpp
System::String textDoc = System::String(u"      Line 1 \n") + u"    Line 2   \n" + u" Line 3       ";

// Créez un objet "TxtLoadOptions", que nous pouvons passer au constructeur d'un document
// pour modifier la façon dont nous chargeons un document texte brut.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Définissez la propriété "LeadingSpacesOptions" sur "TxtLeadingSpacesOptions.Preserve"
// pour conserver tous les caractères d'espacement au début de chaque ligne.
// Définissez la propriété "LeadingSpacesOptions" sur "TxtLeadingSpacesOptions.ConvertToIndent"
// pour supprimer tous les caractères d'espacement du début de chaque ligne,
// et appliquez ensuite un retrait de première ligne à gauche au paragraphe pour simuler l'effet des espaces.
// Définissez la propriété "LeadingSpacesOptions" sur "TxtLeadingSpacesOptions.Trim"
// pour supprimer tous les caractères d'espacement du début de chaque ligne.
loadOptions->set_LeadingSpacesOptions(txtLeadingSpacesOptions);

// Définissez la propriété "TrailingSpacesOptions" sur "TxtTrailingSpacesOptions.Preserve"
// pour conserver tous les caractères d'espacement à la fin de chaque ligne.
// Définissez la propriété "TrailingSpacesOptions" sur "TxtTrailingSpacesOptions.Trim" pour
// supprimer tous les caractères d'espacement de la fin de chaque ligne.
loadOptions->set_TrailingSpacesOptions(txtTrailingSpacesOptions);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

switch (txtLeadingSpacesOptions)
{
    case Aspose::Words::Loading::TxtLeadingSpacesOptions::ConvertToIndent:
        ASPOSE_ASSERT_EQ(37.8, paragraphs->idx_get(0)->get_ParagraphFormat()->get_FirstLineIndent());
        ASPOSE_ASSERT_EQ(25.2, paragraphs->idx_get(1)->get_ParagraphFormat()->get_FirstLineIndent());
        ASPOSE_ASSERT_EQ(6.3, paragraphs->idx_get(2)->get_ParagraphFormat()->get_FirstLineIndent());
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
        break;

    case Aspose::Words::Loading::TxtLeadingSpacesOptions::Preserve:
        ASSERT_TRUE(paragraphs->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
        {
            return (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0;
        }))));
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"      Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"    Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u" Line 3"));
        break;

    case Aspose::Words::Loading::TxtLeadingSpacesOptions::Trim:
        ASSERT_TRUE(paragraphs->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
        {
            return (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0;
        }))));
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
        break;

}

switch (txtTrailingSpacesOptions)
{
    case Aspose::Words::Loading::TxtTrailingSpacesOptions::Preserve:
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1 \r"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2   \r"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3       \f"));
        break;

    case Aspose::Words::Loading::TxtTrailingSpacesOptions::Trim:
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1\r"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2\r"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3\f"));
        break;

}
```

## Voir aussi

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
