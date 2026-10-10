---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText méthode"
linktitle: "get_IsShowingPlaceholderText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText méthode. Spécifie si le contenu de ce SDT doit être interprété comme contenant du texte de substitution (par opposition au texte régulier contenu dans le SDT). Si la valeur est vraie, cet état sera réactivé (affichage du texte de substitution) lors de l'ouverture de ce document en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.markup/structureddocumenttag/get_isshowingplaceholdertext/
---
## StructuredDocumentTag::get_IsShowingPlaceholderText method


Spécifie si le contenu de ce **SDT** doit être interprété comme contenant du texte d'espace réservé (par opposition au texte ordinaire à l'intérieur du SDT). si la valeur est **true**, cet état sera repris (affichage du texte d'espace réservé) à l'ouverture de ce document.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText() override
```


## Exemples



Montre comment utiliser le contenu d'un bloc de construction comme texte d'espace réservé personnalisé pour une balise de document structuré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insérez une balise de document structuré en texte brut du type "PlainText", qui fonctionnera comme une zone de texte.
// Le contenu qu'elle affichera par défaut est l'invite "Cliquez ici pour saisir du texte.".
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Nous pouvons faire en sorte que la balise affiche le contenu d'un bloc de construction au lieu du texte par défaut.
// Tout d'abord, ajoutez un bloc de construction avec du contenu au document de glossaire.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();

auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"Custom Placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(glossaryDoc));
substituteBlock->get_FirstSection()->get_Body()->AppendParagraph(u"Custom placeholder text.");

glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Ensuite, utilisez la propriété "PlaceholderName" de la balise de document structuré pour référencer ce bloc de construction par son nom.
tag->set_PlaceholderName(u"Custom Placeholder");

// Si "PlaceholderName" fait référence à un bloc existant dans le document de glossaire du document parent,
// nous pourrons vérifier le bloc de construction via la propriété "Placeholder".
ASPOSE_ASSERT_EQ(substituteBlock, tag->get_Placeholder());

// Définissez la propriété "IsShowingPlaceholderText" sur "true" pour traiter le
// contenu actuel de la balise de document structuré comme texte d'espace réservé.
// Cela signifie que cliquer sur la zone de texte dans Microsoft Word mettra immédiatement en surbrillance tout le contenu de la balise.
// Définissez la propriété "IsShowingPlaceholderText" sur "false" pour obtenir le
// balise de document structuré afin qu'elle traite son contenu comme du texte déjà saisi par l'utilisateur.
// Cliquer sur ce texte dans Microsoft Word placera le curseur clignotant à l'emplacement cliqué.
tag->set_IsShowingPlaceholderText(isShowingPlaceholderText);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

## Voir aussi

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
