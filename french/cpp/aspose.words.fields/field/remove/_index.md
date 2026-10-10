---
title: "Aspose::Words::Fields::Field::Remove méthode"
linktitle: "Supprimer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::Field::Remove méthode. Supprime le champ du document. Retourne un nœud immédiatement après le champ. Si la fin du champ est le dernier enfant de son nœud parent, retourne le paragraphe parent. Si le champ est déjà supprimé, retourne null en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words.fields/field/remove/
---
## Field::Remove method


Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**.

```cpp
virtual System::SharedPtr<Aspose::Words::Node> Aspose::Words::Fields::Field::Remove()
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

* Class [Node](../../../aspose.words/node/)
* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
