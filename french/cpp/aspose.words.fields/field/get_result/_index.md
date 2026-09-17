---
title: "Aspose::Words::Fields::Field::get_Result méthode"
linktitle: "get_Result"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::Field::get_Result méthode. Obtient ou définit le texte situé entre le séparateur de champ et la fin du champ en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.fields/field/get_result/
---
## Field::get_Result method


Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ.

```cpp
System::String Aspose::Words::Fields::Field::get_Result()
```


## Exemples



Montre comment insérer un champ dans un document à l'aide d'un code de champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Cette surcharge de la méthode InsertField met automatiquement à jour les champs insérés.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Voir aussi

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
