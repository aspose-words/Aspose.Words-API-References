---
title: "Aspose::Words::Body::EnsureMinimum méthode"
linktitle: "EnsureMinimum"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Body::EnsureMinimum méthode. Si le dernier enfant n'est pas un paragraphe, crée et ajoute un paragraphe vide en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/body/ensureminimum/
---
## Body::EnsureMinimum method


Si le dernier enfant n’est pas un paragraphe, crée et ajoute un paragraphe vide.

```cpp
void Aspose::Words::Body::EnsureMinimum()
```


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

* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
