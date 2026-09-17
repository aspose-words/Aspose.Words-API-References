---
title: "Classe Aspose::Words::Range"
linktitle: "Plage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Range. Représente une zone contiguë dans un document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 51000
url: /fr/cpp/aspose.words/range/
---
## Range class


Représente une zone contiguë dans un document. Pour en savoir plus, consultez l'article de documentation [Working with Ranges](https://docs.aspose.com/words/cpp/working-with-ranges/).

```cpp
class Range : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Delete](./delete/)() | Supprime tous les caractères de la plage. |
| [get_Bookmarks](./get_bookmarks/)() | Renvoie une collection [Bookmarks](./get_bookmarks/) qui représente tous les signets dans la plage. |
| [get_Fields](./get_fields/)() | Renvoie une collection [Fields](./get_fields/) qui représente tous les champs dans la plage. |
| [get_FormFields](./get_formfields/)() | Renvoie une collection [FormFields](./get_formfields/) qui représente tous les champs de formulaire dans la plage. |
| [get_Revisions](./get_revisions/)() | Obtient une collection de révisions (modifications suivies) qui existent dans cette plage. |
| [get_StructuredDocumentTags](./get_structureddocumenttags/)() | Renvoie une collection [StructuredDocumentTags](./get_structureddocumenttags/) qui représente toutes les balises de document structurées dans la plage. |
| [get_Text](./get_text/)() | Obtient le texte de la plage. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Modifie les valeurs du type de champ [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) de [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/) et [FieldEnd](../../aspose.words.fields/fieldend/) dans cette plage afin qu'elles correspondent aux types de champ contenus dans les codes de champ. |
| [Replace](./replace/)(const System::String\&, const System::String\&) | Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Remplace toutes les occurrences d'un motif de caractères spécifié par une expression régulière par une autre chaîne. |
| [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Remplace toutes les occurrences d'un motif de caractères spécifié par une expression régulière par une autre chaîne. |
| [ToDocument](./todocument/)() | Construit un nouveau document complet qui contient la plage. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Délie les champs dans cette plage. |
| [UpdateFields](./updatefields/)() | Met à jour les valeurs des champs du document dans cette plage. |
## Remarques


Le document est représenté par un arbre de nœuds et les nœuds offrent des opérations pour travailler avec l'arbre, mais certaines opérations sont plus faciles à réaliser si le document est traité comme une séquence contiguë de texte.

[Range](./) is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

[Range](./) does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

## Exemples



Montre comment obtenir le contenu texte de tous les nœuds couverts par une plage.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
