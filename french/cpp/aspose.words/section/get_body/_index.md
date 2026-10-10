---
title: "Méthode Aspose::Words::Section::get_Body"
linktitle: "get_Body"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Section::get_Body. Retourne le nœud enfant Body de la section en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words/section/get_body/
---
## Section::get_Body method


Retourne le nœud enfant [Body](../../body/) de la section.

```cpp
System::SharedPtr<Aspose::Words::Body> Aspose::Words::Section::get_Body()
```

## Remarques


[Body](../../body/) contains main text of the section.

Retourne **null** si la section ne possède pas de nœud [Body](../../body/) parmi ses enfants.

## Exemples



Efface le texte principal de toutes les sections du document en laissant les sections elles‑mêmes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un document vierge contient une section, un corps et un paragraphe.
// Appelez la méthode "RemoveAllChildren" pour supprimer tous ces nœuds,
// et obtenez un nœud de document sans enfants.
doc->RemoveAllChildren();

// Ce document n’a maintenant aucun nœud enfant composite auquel nous puissions ajouter du contenu.
// Si nous souhaitons le modifier, nous devrons reconstituer sa collection de nœuds.
// Tout d’abord, créez une nouvelle section, puis ajoutez-la en tant qu’enfant au nœud racine du document.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Une section nécessite un corps, qui contiendra et affichera tout son contenu
// sur la page entre l’en-tête et le pied-de-page de la section.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Ce corps n'a aucun enfant, nous ne pouvons donc pas encore y ajouter de runs.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Appelez "EnsureMinimum" pour vous assurer que ce corps contient au moins un paragraphe vide.
body->EnsureMinimum();

// Maintenant, nous pouvons ajouter des runs au corps, et faire afficher le document.
body->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Voir aussi

* Class [Body](../../body/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
