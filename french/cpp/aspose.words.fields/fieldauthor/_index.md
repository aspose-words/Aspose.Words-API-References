---
title: "classe Aspose::Words::Fields::FieldAuthor"
linktitle: "FieldAuthor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Fields::FieldAuthor. Implémente le champ AUTHOR. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.fields/fieldauthor/
---
## FieldAuthor class


Implémente le champ AUTHOR. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldAuthor : public Aspose::Words::Fields::Field
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AuthorName](./get_authorname/)() | Obtient ou définit le nom de l'auteur du document. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_AuthorName](./set_authorname/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldAuthor::get_AuthorName](./get_authorname/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |

## Exemples



Montre comment utiliser un champ AUTHOR pour afficher le nom du créateur du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les champs AUTHOR tirent leurs résultats de la propriété intégrée du document appelée "Author".
// Si nous créons et enregistrons un document dans Microsoft Word,
// il contiendra notre nom d'utilisateur dans cette propriété.
// Cependant, si nous créons un document de manière programmatique en utilisant Aspose.Words,
// la propriété "Author", par défaut, sera une chaîne vide.
ASSERT_EQ(System::String::Empty, doc->get_BuiltInDocumentProperties()->get_Author());

// Définissez un nom d'auteur de secours à utiliser par les champs AUTHOR
// si la propriété "Author" contient une chaîne vide.
doc->get_FieldOptions()->set_DefaultDocumentAuthor(u"Joe Bloggs");

builder->Write(u"This document was created by ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"Joe Bloggs", field->get_Result());

// Mise à jour d'un champ AUTHOR contenant une valeur
// appliquera cette valeur à la propriété intégrée "Author".
ASSERT_EQ(u"Joe Bloggs", doc->get_BuiltInDocumentProperties()->get_Author());

// Modifier cette propriété, puis mettre à jour le champ AUTHOR appliquera cette valeur au champ.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"John Doe", field->get_Result());

// Si nous mettons à jour un champ AUTHOR après avoir modifié sa propriété "Name",
// alors le champ affichera le nouveau nom et appliquera le nouveau nom à la propriété intégrée.
field->set_AuthorName(u"Jane Doe");
field->Update();

ASSERT_EQ(u" AUTHOR  \"Jane Doe\"", field->GetFieldCode());
ASSERT_EQ(u"Jane Doe", field->get_Result());

// Les champs AUTHOR n'affectent pas la propriété DefaultDocumentAuthor.
ASSERT_EQ(u"Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Joe Bloggs", doc->get_FieldOptions()->get_DefaultDocumentAuthor());

doc->Save(get_ArtifactsDir() + u"Field.AUTHOR.docx");
```

## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
