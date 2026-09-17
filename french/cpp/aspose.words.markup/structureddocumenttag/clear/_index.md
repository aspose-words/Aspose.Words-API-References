---
title: "Méthode Clear de Aspose::Words::Markup::StructuredDocumentTag"
linktitle: "Clear"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Clear de Aspose::Words::Markup::StructuredDocumentTag. Efface le contenu de cette balise de document structuré et affiche un espace réservé s'il est défini en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag::Clear method


Efface le contenu de cette balise de document structuré et affiche un espace réservé s'il est défini.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::Clear()
```

## Remarques


Il n'est pas possible d'effacer le contenu d'une balise de document structuré si elle possède des révisions.

Si cette balise de document structuré est mappée à du XML personnalisé (en utilisant la propriété [XmlMapping](../get_xmlmapping/)), le nœud XML référencé est effacé.

## Exemples



Montre comment supprimer le contenu des éléments de balise de document structuré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créez une balise de document structuré en texte brut, puis ajoutez‑la au document.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Cette balise de document structuré, qui est sous forme de zone de texte, affiche déjà le texte de l'espace réservé.
ASSERT_EQ(u"Click here to enter text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Créez un bloc de construction avec du texte.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();
auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"My placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->EnsureMinimum();
substituteBlock->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(glossaryDoc, u"Custom placeholder text."));
glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Définissez la propriété "PlaceholderName" de la balise de document structuré sur le nom de notre bloc de construction pour obtenir
// la balise de document structuré afin d'afficher le contenu du bloc de construction à la place du texte par défaut original.
tag->set_PlaceholderName(u"My placeholder");

ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Modifiez le texte de la balise de document structuré et masquez le texte de l'espace réservé.
auto run = System::ExplicitCast<Aspose::Words::Run>(tag->GetChild(Aspose::Words::NodeType::Run, 0, true));
run->set_Text(u"New text.");
tag->set_IsShowingPlaceholderText(false);

ASSERT_EQ(u"New text.", tag->GetText().Trim());

// Utilisez la méthode "Clear" pour effacer le contenu de cette balise de document structuré et afficher à nouveau l'espace réservé.
tag->Clear();

ASSERT_TRUE(tag->get_IsShowingPlaceholderText());
ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
```

## Voir aussi

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
