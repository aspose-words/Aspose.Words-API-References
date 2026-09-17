---
title: "Méthode Aspose::Words::Fields::FieldChar::get_IsLocked"
linktitle: "get_IsLocked"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldChar::get_IsLocked. Obtient ou définit si le champ parent est verrouillé (ne doit pas recalculer son résultat) en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fields/fieldchar/get_islocked/
---
## FieldChar::get_IsLocked method


Obtient ou définit si le champ parent est verrouillé (ne doit pas recalculer son résultat).

```cpp
bool Aspose::Words::Fields::FieldChar::get_IsLocked() const
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

* Class [FieldChar](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
