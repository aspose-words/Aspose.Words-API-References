---
title: "Méthode Aspose::Words::Fields::Field::GetFieldCode"
linktitle: "GetFieldCode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::Field::GetFieldCode. Retourne le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat du champ des champs enfants sont inclus en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.fields/field/getfieldcode/
---
## Field::GetFieldCode() method


Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus.

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode()
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


Montre comment obtenir le code d'un champ.
```cpp
// Ouvrez un document qui contient un MERGEFIELD à l'intérieur d'un champ IF.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Il existe deux façons d'obtenir le code de champ du champ :
// 1 -  Omettre ses champs internes :
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Inclure ses champs internes :
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Par défaut, la méthode GetFieldCode affiche les champs internes.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Voir aussi

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::GetFieldCode(bool) method


Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur).

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode(bool includeChildFieldCodes)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | bool | **true** si les codes de champ enfants doivent être inclus. |

## Exemples



Montre comment obtenir le code d'un champ.
```cpp
// Ouvrez un document qui contient un MERGEFIELD à l'intérieur d'un champ IF.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Il existe deux façons d'obtenir le code de champ du champ :
// 1 -  Omettre ses champs internes :
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Inclure ses champs internes :
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Par défaut, la méthode GetFieldCode affiche les champs internes.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Voir aussi

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
