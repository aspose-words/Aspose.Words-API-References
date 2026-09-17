---
title: "Méthode Aspose::Words::Fields::FieldChar::get_FieldType"
linktitle: "get_FieldType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldChar::get_FieldType. Retourne le type du champ en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldchar/get_fieldtype/
---
## FieldChar::get_FieldType method


Renvoie le type du champ.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FieldChar::get_FieldType() const
```


## Exemples



Montre comment travailler avec un nœud [FieldStart](../../fieldstart/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

System::SharedPtr<Aspose::Words::Fields::FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// Récupérez l'objet façade qui représente le champ dans le document.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Mettez à jour le champ pour afficher la date actuelle.
field->Update();
```

## Voir aussi

* Enum [FieldType](../../fieldtype/)
* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
