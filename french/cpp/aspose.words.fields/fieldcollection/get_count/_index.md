---
title: "Aspose::Words::Fields::FieldCollection::get_Count méthode"
linktitle: "get_Count"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldCollection::get_Count méthode. Retourne le nombre de champs dans la collection en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldcollection/get_count/
---
## FieldCollection::get_Count method


Renvoie le nombre de champs dans la collection.

```cpp
int32_t Aspose::Words::Fields::FieldCollection::get_Count()
```


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

* Class [FieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
