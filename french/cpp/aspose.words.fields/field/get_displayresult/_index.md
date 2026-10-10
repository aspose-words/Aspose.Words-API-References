---
title: "Aspose::Words::Fields::Field::get_DisplayResult méthode"
linktitle: "get_DisplayResult"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::Field::get_DisplayResult méthode. Obtient le texte qui représente le résultat affiché du champ en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/field/get_displayresult/
---
## Field::get_DisplayResult method


Obtient le texte qui représente le résultat du champ affiché.

```cpp
System::String Aspose::Words::Fields::Field::get_DisplayResult()
```


## Exemples



Montre comment obtenir le texte réel qu'un champ affiche dans le document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This document was written by ");
auto fieldAuthor = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
fieldAuthor->set_AuthorName(u"John Doe");

// Nous pouvons utiliser la propriété DisplayResult pour vérifier quel texte exact
// un champ afficherait à sa place dans le document.
ASSERT_EQ(System::String::Empty, fieldAuthor->get_DisplayResult());

// Les champs ne conservent pas de valeurs de résultat précises en temps réel.
// Pour s'assurer que nos champs affichent des résultats précis à tout moment,
// comme juste avant une opération d'enregistrement, nous devons les mettre à jour manuellement.
fieldAuthor->Update();

ASSERT_EQ(u"John Doe", fieldAuthor->get_DisplayResult());

doc->Save(get_ArtifactsDir() + u"Field.DisplayResult.docx");
```

## Voir aussi

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
