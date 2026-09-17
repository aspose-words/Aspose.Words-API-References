---
title: "Classe Aspose::Words::Fields::FieldCollection"
linktitle: "FieldCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldCollection class. Une collection d'objets Field qui représente les champs dans la plage spécifiée. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 23000
url: /fr/cpp/aspose.words.fields/fieldcollection/
---
## FieldCollection class


Une collection d'objets [Field](../field/) qui représente les champs dans la plage spécifiée. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::Field>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clear](./clear/)() | Supprime tous les champs de cette collection du document et de la collection elle‑même. |
| [get_Count](./get_count/)() | Renvoie le nombre de champs dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Renvoie un champ à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&) | Supprime le champ spécifié de cette collection et du document. |
| [RemoveAt](./removeat/)(int32_t) | Supprime un champ à l'index spécifié de cette collection et du document. |
| static [Type](./type/)() |  |
## Remarques


Une instance de cette collection parcourt les champs qui commencent et se situent dans la plage spécifiée.

La collection [FieldCollection](./) ne possède pas les champs qu'elle contient, elle n'est qu'une sélection de champs.

La collection [FieldCollection](./) est « live », c’est‑à‑dire que les modifications apportées aux enfants de l’objet nœud à partir duquel elle a été créée sont immédiatement reflétées dans les champs renvoyés par les propriétés et méthodes de [FieldCollection](./).

## Exemples



Montre comment supprimer des champs d’une collection de champs.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder->InsertField(u" TIME ");
builder->InsertField(u" REVNUM ");
builder->InsertField(u" AUTHOR  \"John Doe\" ");
builder->InsertField(u" SUBJECT \"My Subject\" ");
builder->InsertField(u" QUOTE \"Hello world!\" ");
doc->UpdateFields();

System::SharedPtr<Aspose::Words::Fields::FieldCollection> fields = doc->get_Range()->get_Fields();

ASSERT_EQ(6, fields->get_Count());

// Voici quatre façons de supprimer des champs d’une collection de champs.
// 1 -  Obtenir un champ pour qu’il se supprime lui‑même :
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  Faire appel à la collection pour supprimer un champ que nous lui transmettons via sa méthode de suppression :
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  Supprimer un champ d’une collection à un index :
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  Supprimer tous les champs de la collection en une seule fois :
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
