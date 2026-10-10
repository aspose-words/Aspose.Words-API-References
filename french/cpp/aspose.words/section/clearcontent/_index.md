---
title: "Méthode Aspose::Words::Section::ClearContent"
linktitle: "ClearContent"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Section::ClearContent. Efface la section en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/section/clearcontent/
---
## Section::ClearContent method


Efface la section.

```cpp
void Aspose::Words::Section::ClearContent()
```

## Remarques


Le texte de [Body](../get_body/) est effacé, il ne reste qu'un paragraphe vide qui représente le saut de section.

Le texte de tous les en-têtes et pieds de page est effacé, mais les objets [HeaderFooter](../../headerfooter/) eux‑mêmes ne sont pas supprimés.

## Exemples



Montre comment effacer le contenu d'une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// L'exécution de la méthode "ClearContent" supprimera tout le contenu de la section
// mais laissera un paragraphe vide pour ajouter du contenu à nouveau.
doc->get_FirstSection()->ClearContent();

ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
```

## Voir aussi

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
